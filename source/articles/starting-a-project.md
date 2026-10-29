# Starting well: stakeholders and the project charter

**Covers:** Stakeholder mapping, Project charter

## The first week decides a lot {#overview}
Most projects that fail did not fail in the code. They failed because someone important was not consulted, or because people had different pictures of what the project was meant to do. Two short activities at the start prevent most of this: find out who has a stake in the result, and write down what the project is for. Both take hours, not weeks.

## Stakeholder mapping {#stakeholder-mapping}
Stakeholder mapping is identifying everyone who has a real stake in the project's outcome, before you plan around them. The obvious names are the sponsor who pays and the developers who build. The less obvious ones are often more important: the support team that will receive the calls, the legal department that must approve, the customers who will use it and the other team whose system yours depends on.

A common way to organize them is a grid with two axes, power and interest:

| | Low interest | High interest |
|---|---|---|
| **High power** | Keep satisfied | Manage closely |
| **Low power** | Monitor | Keep informed |

Each box suggests how often to talk to those people and about what. Someone with high power and high interest, like the sponsor, needs regular conversations. Someone with high power and low interest, like a security reviewer, needs to be kept satisfied and consulted at the right moment, so they do not block you late.

Revisit the map as the project goes on, because people's interest and influence change.

## Project charter {#project-charter}
A project charter is a short document, written before real work begins, that states the project's purpose, its goals and its boundaries. Its job is to make sure that everyone starts from the same shared understanding of what the project is and is not.

A useful charter fits on one or two pages and covers:
- **Purpose:** the problem and why it matters now.
- **Goals:** measurable results that show success.
- **Scope:** what is included and what is explicitly left out.
- **Stakeholders and roles:** who decides, who builds and who is consulted.
- **Time and budget:** the rough limits.
- **Risks and assumptions:** what could go wrong and what you are taking for granted.

The sponsor signs it, which gives the project manager authority and a document to point to when requests start to drift. The "out of scope" list is often the most valuable part.

## A worked example {#example}
A company wants a customer portal. Here is how the two tools work together.

1. List stakeholders: the sales director (sponsor), 3 developers, the support team, the legal team, the finance team that handles invoices, and about 500 customers.
2. Place them on the grid. Sales director: high power, high interest, so manage closely. Legal: high power, low interest, so keep satisfied and ask for review early. Support: low power, high interest, so keep informed. Customers: low power, high interest, so interview a sample.
3. Write the charter:

| Section | Entry |
|---|---|
| Purpose | Customers call support to ask for invoices, which costs 40 hours a week |
| Goal | Cut invoice calls by 50 percent within 3 months of launch |
| In scope | View and download invoices |
| Out of scope | Online payment, mobile app |
| Budget and time | 6 weeks, 3 developers |
| Risk | Legal approval for storing invoices online |

The goal can be checked: 40 hours a week falling by half is 20 hours. The charter also settles an argument in advance: when someone asks for online payment in week 4, the team points to the out-of-scope line and raises a formal change instead.

## A common mistake {#mistake}
Mapping only the people who are easy to see. Quiet stakeholders, such as the team that runs the servers, can stop a launch at the last minute. A second mistake is a long charter that nobody reads. If it takes more than two pages, no one will remember it.

## Key points {#key-points}
- Stakeholder mapping finds everyone with a stake, and the power and interest grid guides how to involve them.
- A project charter states purpose, goals and boundaries on a page or two.
- Write the out-of-scope list. It prevents arguments later.
- Review both documents as the project changes.
