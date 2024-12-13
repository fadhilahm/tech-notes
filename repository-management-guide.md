# Managing Repository for Teams: A Practical Introduction

## Introduction

Hi! I'm Fadhilah Metra, a full-stack developer at e-dash. Through my 4 years of experience in startups and small companies, I've learned how important repository management is for team development. In this article, I'll share practical knowledge about managing repositories effectively, focusing on real-world scenarios that development teams commonly face.

## Why is Repository Management Important?

Repository management is essential in modern software development for these key reasons:

1. **Smooth Collaboration** 
   - Multiple developers can work on the same codebase without stepping on each other's toes
   - Teams can work on different features simultaneously
   - Changes are tracked and can be reviewed by team members

2. **Reduced Conflicts and Errors**
   - Prevent conflicts when different developers edit the same files
   - Early detection of integration issues
   - Easier to identify and fix bugs through version history

3. **Better Code Quality**
   - Facilitates code review processes
   - Ensures consistent coding standards
   - Makes it easier to maintain clean, organized code

## Repository Structures

When setting up your development environment, you'll need to choose between two main repository structures. Here's a detailed look at each:

### 1. Multi-repository
```
company-projects/
├── project-a/ <-- separate repository
│   ├── src/
│   ├── tests/
│   └── docs/
│
├── project-b/ <-- separate repository
│   ├── src/
│   ├── tests/
│   └── docs/
│
└── project-c/ <-- separate repository
    ├── src/
    ├── tests/
    └── docs/
```

**Advantages:**
- Clear separation between projects
- Teams can work independently
- Easier to manage access permissions
- Smaller, more focused codebases

**Common Use Cases:**
- Microservices architecture
- Projects with different technology stacks
- Teams working on distinct products

### 2. Mono-repository
```
company-monorepo/ <-- single repository
├── project-a/
│   ├── src/
│   ├── tests/
│   └── docs/
│
├── project-b/
│   ├── src/
│   ├── tests/
│   └── docs/
│
└── project-c/
    ├── src/
    ├── tests/
    └── docs/
```

**Advantages:**
- Easier code sharing and reuse
- Single source of truth
- Simplified dependency management
- Coordinated changes across projects

**Common Use Cases:**
- Tightly coupled services
- Projects sharing lots of code
- Small to medium-sized teams

## Branching Strategies

Let's explore three effective branching strategies and when to use each one:

### 1. Trunk-based Development
Best for small teams that needs to create new features or MVP quickly.

<p align="center">
   <img src="./assets/trunk-based_development.png" height="400">
</p>

### 2. Feature Branching
Perfect for teams working on multiple features simultaneously.

<p align="center">
   <img src="./assets/feature_branching.png" height="400">
</p>

### 3. Git Flow
Suitable for projects with scheduled releases.

<p align="center">
   <img src="./assets/git_flow.svg" height="400">
</p>

## Code Reviews and Pull Requests

Good code reviews are crucial for maintaining code quality. The key is to keep your changes focused and your PRs small and clear.

### ❌ Example of a Hard-to-Review Pull Request:
```markdown
Title: Update User System

Description:
This PR:
- Adds user profile management
- Implements new authentication
- Updates email system
- Adds avatar upload
- Changes database schema
- Implements privacy settings
- Updates API documentation
- Adds unit tests for all changes
- Updates frontend components
- Implements caching system

[... 50+ files changed ...]
```

### ✅ Example of a Good Pull Request:
```markdown
Title: Add User Profile Image Upload

Description:
Implements user avatar upload functionality with size and format validation.

Changes:
- Add image upload component
- Add size and format validation (max 2MB, jpg/png)
- Add unit tests for validation logic

Screenshots:
[Upload component screenshot]

Testing:
- [x] Image upload success
- [x] Size validation
- [x] Format validation
- [x] Error handling

Note: This is part 1 of the profile update feature. Following PRs will handle storage and display.
```

### Why Small PRs are Better:
- Easier to review thoroughly
- Faster to merge
- Lower risk of conflicts
- Quicker feedback cycle
- Simpler to revert if needed

### Tips for Better PRs:
1. One feature or fix per PR
2. Clear, focused description of changes
3. Include relevant tests only
4. Add screenshots for UI changes

## Collaboration Tools

A well-configured toolset makes repository management much easier:

1. **Version Control Platforms**
   - GitHub/GitLab
   - Use cases:
     * Code hosting and version control
     * Pull request management
     * Code review discussions
     * Issue tracking
     * Project documentation

2. **Communication Tools**
   - Slack/Teams
   - Use cases:
     * Code review notifications
     * Team discussions
     * Integration with Git platforms
     * Quick problem-solving sessions

3. **Documentation Systems**
   - Notion/Confluence
   - Use cases:
     * Technical documentation
     * Development guidelines
     * Architecture decisions
     * Onboarding materials

4. **CI/CD Tools**
   - Jenkins/GitHub Actions
   - Use cases:
     * Automated testing
     * Build processes
     * Deployment automation

## Conclusion

Repository management is a fundamental skill in modern software development. While it might seem overwhelming at first, starting with these basics and gradually improving your workflow will lead to more efficient team collaboration.

Remember that the goal is to find what works best for your team. Start with these foundations and adjust based on your team's needs and feedback.
