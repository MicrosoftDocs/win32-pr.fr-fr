---
description: Cette rubrique contient des informations sur l’écriture d’un analyseur de protocole et inclut des exemples de fonctions d’exportation que la DLL de l’analyseur doit implémenter.
ms.assetid: 0be87b33-aab0-4986-8a86-914e0a7b8f2d
title: Écriture d’un analyseur de protocole
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338c224dd036df747af6ab805dae273f6ad3f510
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528732"
---
# <a name="writing-a-protocol-parser"></a><span data-ttu-id="1471a-103">Écriture d’un analyseur de protocole</span><span class="sxs-lookup"><span data-stu-id="1471a-103">Writing a Protocol Parser</span></span>

<span data-ttu-id="1471a-104">Cette rubrique contient des informations sur l’écriture d’un analyseur de protocole et inclut des exemples de fonctions d’exportation que la DLL de l’analyseur doit implémenter.</span><span class="sxs-lookup"><span data-stu-id="1471a-104">This topic contains information about writing a protocol parser, and includes examples of the export functions that the parser DLL must implement.</span></span>

<span data-ttu-id="1471a-105">Les rubriques suivantes sont incluses dans cette section.</span><span class="sxs-lookup"><span data-stu-id="1471a-105">The following topics are included in this section.</span></span>



| <span data-ttu-id="1471a-106">Terme</span><span class="sxs-lookup"><span data-stu-id="1471a-106">Term</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="1471a-107">Description</span><span class="sxs-lookup"><span data-stu-id="1471a-107">Description</span></span>                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1471a-108"><span id="Programming_Considerations"></span><span id="programming_considerations"></span><span id="PROGRAMMING_CONSIDERATIONS"></span>[Considérations relatives à la programmation](programming-considerations.md)</span><span class="sxs-lookup"><span data-stu-id="1471a-108"><span id="Programming_Considerations"></span><span id="programming_considerations"></span><span id="PROGRAMMING_CONSIDERATIONS"></span>[Programming Considerations](programming-considerations.md)</span></span><br/>                                                   | <span data-ttu-id="1471a-109">Identifie les conseils de programmation de base pour vous aider à écrire une DLL d’analyseur.</span><span class="sxs-lookup"><span data-stu-id="1471a-109">Identifies the basic programming tips to help you write a parser DLL.</span></span><br/>                                                                                    |
| <span data-ttu-id="1471a-110"><span id="Implementing_Parser_Export_Functions"></span><span id="implementing_parser_export_functions"></span><span id="IMPLEMENTING_PARSER_EXPORT_FUNCTIONS"></span>[Implémentation des fonctions d’exportation de l’analyseur](implementing-parser-export-functions.md)</span><span class="sxs-lookup"><span data-stu-id="1471a-110"><span id="Implementing_Parser_Export_Functions"></span><span id="implementing_parser_export_functions"></span><span id="IMPLEMENTING_PARSER_EXPORT_FUNCTIONS"></span>[Implementing Parser Export Functions](implementing-parser-export-functions.md)</span></span><br/> | <span data-ttu-id="1471a-111">Fournit des exemples d’implémentation de fonctions d’exportation.</span><span class="sxs-lookup"><span data-stu-id="1471a-111">Provides examples of implementing export functions.</span></span><br/>                                                                                                      |
| <span data-ttu-id="1471a-112"><span id="Formatting_Displayed_Data"></span><span id="formatting_displayed_data"></span><span id="FORMATTING_DISPLAYED_DATA"></span>[Mise en forme des données affichées](formatting-displayed-data.md)</span><span class="sxs-lookup"><span data-stu-id="1471a-112"><span id="Formatting_Displayed_Data"></span><span id="formatting_displayed_data"></span><span id="FORMATTING_DISPLAYED_DATA"></span>[Formatting Displayed Data](formatting-displayed-data.md)</span></span><br/>                                                        | <span data-ttu-id="1471a-113">Identifie le processus de mise en forme des données affichées dans le volet d’informations de l’interface utilisateur Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="1471a-113">Identifies the process of formatting data that is displayed in the details pane of the Network Monitor UI.</span></span><br/>                                               |
| <span data-ttu-id="1471a-114"><span id="Specifying_a_Follow_Set"></span><span id="specifying_a_follow_set"></span><span id="SPECIFYING_A_FOLLOW_SET"></span>[Spécification d’un jeu de suivi](specifying-a-follow-set.md)</span><span class="sxs-lookup"><span data-stu-id="1471a-114"><span id="Specifying_a_Follow_Set"></span><span id="specifying_a_follow_set"></span><span id="SPECIFYING_A_FOLLOW_SET"></span>[Specifying a Follow Set](specifying-a-follow-set.md)</span></span><br/>                                                                  | <span data-ttu-id="1471a-115">Identifie le processus de spécification d’un jeu de suivi et vous montre comment Moniteur réseau accède au jeu suivant d’un analyseur pour déterminer le protocole suivant.</span><span class="sxs-lookup"><span data-stu-id="1471a-115">Identifies the process of specifying a follow set, and shows you how Network Monitor accesses the follow set of a parser to determine the next protocol.</span></span><br/> |
| <span data-ttu-id="1471a-116"><span id="Specifying_a_Handoff_Set"></span><span id="specifying_a_handoff_set"></span><span id="SPECIFYING_A_HANDOFF_SET"></span>[Spécification d’un jeu de remise](specifying-a-handoff-set.md)</span><span class="sxs-lookup"><span data-stu-id="1471a-116"><span id="Specifying_a_Handoff_Set"></span><span id="specifying_a_handoff_set"></span><span id="SPECIFYING_A_HANDOFF_SET"></span>[Specifying a Handoff Set](specifying-a-handoff-set.md)</span></span><br/>                                                             | <span data-ttu-id="1471a-117">Identifie le processus de spécification d’un jeu de remise et vous montre comment l’analyseur accède à son jeu de remise pour obtenir un handle vers le protocole suivant.</span><span class="sxs-lookup"><span data-stu-id="1471a-117">Identifies the process of specifying a handoff set, and shows you how the parser accesses its handoff set to get a handle to the next protocol.</span></span><br/>          |



 

 

 




