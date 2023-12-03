---
title: "Blockchain based Healthcare Transaction System"
collection: projects
---

<style>
  a 
  {
    color: blue;
    text-decoration: none;
  }
</style>

<a style="text-decoration: none;" href="/files/Healthcare_Blockchain_Project_Presentation.pdf">[Presentation]</a>

## Problem Statement

 * An excessive amount of patient records are stored in paper format and the process to update/transfer when a patient switches to new doctors/hospitals is quite tedious and inefficient.
 * The retrieval of necessary blood/organs in the shortest possible time is of utmost importance when actual lives are at stake. Organ/Blood donation transactions have always been cumbersome and inefficient.
 * The entire process of the transaction involving contacting and trying to find the availability of organs/blood with several vendors/hospitals (coupled with the possibility of missing out on unknown contacts) and filling the necessary transaction details/paperwork is laborious, slow and ineffective.
 * The costs involved in organ/blood donation transactions is oftentimes unimaginably expensive and involves substantial intermediate costs that should be eliminated.
 * The process of transaction is not a very transparent one and it often involves dishonest and malicious intent and underhand dealings which should be prevented at all costs.
 * It is imperative that these processes are made more efficient and transparent given that it is a matter of life and death.

## Our Solution

The project addressed and solved the above problems by implementing a solution in the following manner:
 * The patient records are stored in a digitalised, decentralized, transparent and secure manner using the revolutionary technology of blockchain
 * All the details necessary for organ/blood transactions are also stored in the format of blockchains, enabling clean and hassle-free experiences
 * A Progressive Web Application (PWA) is used by:
    * The patients to view their health records with respective timestamps
    * The hospitals to view patient’s complete medical history
    * The hospitals to query information about available organs/blood across all vendors/donation banks that are a part of the network, and carry out the transaction
 
The above-mentioned solution addresses and solves the various problems that are inherent to the healthcare industry related to the management of patient records and the transaction of blood and organs in the following manner:
 * A completely decentralized system with data stored cryptographically ensures that the data is only accessible with the right permissions
 * Data stored in the form of blockchains are immutable, implying that it cannot be tampered with by anyone for malicious purposes
 * This is a more efficient way for large hospitals to manage thousands of patient records with years of history, thereby enabling better diagnosis and treatment
 * Through the use of Blockchain, all the intermediate transaction costs between the hospitals and the donation banks are eliminated since all the transactions are completely free and transparent (the complete history of any transaction is available to everyone)
 * Transactions are confirmed based on the availability and not based on the name of the hospital or any such preferred choices which would otherwise lead to unfair bias
 * As any transaction can be viewed, it makes pricing transparent and thus prevents horrendous price tags and the resultant exploitation of the helpless patients (which is quite common especially in times of emergencies)

## Implementation Details

 * The project involved the implementation of a custom blockchain from scratch using NodeJS and nodemon and used custom RSA encryption and decryption algorithms to store the data securely. This secure custom blockchain exhibited the features of a typical blockchain and was used as the primary network and storage medium for the healthcare records and the organ/blood donation.
 * The use of a public ledger and implementation of nodes adopting the longest available chain ensured the secure storage of all the relevant data. This makes tampering with the data almost impossible due to the high computation power required by a maliciously motivated entity to solve the complex mathematical problem faster than the rest of the network.
 * The project also involved the implementation of a front-end website that can be used by the hospitals and patients alike to access and retrieve the healthcare records securely and to participate in transparent organ/blood donation transactions.
