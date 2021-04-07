---
title: Implémentation du jeu de propriétés d’informations de résumé
description: Il existe des instructions à suivre lors de l’implémentation d’un jeu de propriétés d’informations de synthèse pour le stockage structuré.
ms.assetid: e1204de5-b712-4bd5-bffb-6a12ec8d7052
keywords:
- Implémentation du jeu de propriétés d’informations de résumé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69e5ae6208aa5cb7a325d1cccf77f17e969c5b75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671066"
---
# <a name="implementing-the-summary-information-property-set"></a><span data-ttu-id="70e27-104">Implémentation du jeu de propriétés d’informations de résumé</span><span class="sxs-lookup"><span data-stu-id="70e27-104">Implementing the Summary Information Property Set</span></span>

<span data-ttu-id="70e27-105">Il existe des instructions à suivre lors de l’implémentation d’un jeu de propriétés d’informations de synthèse pour le stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="70e27-105">There are guidelines to follow when implementing a summary information property set for Structured Storage.</span></span>

<span data-ttu-id="70e27-106">Voici les instructions à suivre pour implémenter [le jeu de propriétés d’informations de résumé](the-summary-information-property-set.md):</span><span class="sxs-lookup"><span data-stu-id="70e27-106">The following are the guidelines for implementing [The Summary Information Property Set](the-summary-information-property-set.md):</span></span>

-   <span data-ttu-id="70e27-107">**PID \_ Le modèle** fait référence à un document externe contenant des informations de format et de style.</span><span class="sxs-lookup"><span data-stu-id="70e27-107">**PID\_TEMPLATE** refers to an external document containing format and style information.</span></span> <span data-ttu-id="70e27-108">Le processus par lequel se trouve le modèle est défini par l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="70e27-108">The process by which the template is located is implementation-defined.</span></span>
-   <span data-ttu-id="70e27-109">**PID \_ LASTAUTHOR** est le nom stocké dans les informations utilisateur par l’application.</span><span class="sxs-lookup"><span data-stu-id="70e27-109">**PID\_LASTAUTHOR** is the name stored in User Information by the application.</span></span> <span data-ttu-id="70e27-110">Par exemple, Mary crée un document sur son ordinateur et le remet à John, qui le modifie et l’enregistre.</span><span class="sxs-lookup"><span data-stu-id="70e27-110">For example, Mary creates a document on her computer and gives it to John, who then modifies and saves it.</span></span> <span data-ttu-id="70e27-111">Mary est l’auteur, John est le dernier enregistré par valeur.</span><span class="sxs-lookup"><span data-stu-id="70e27-111">Mary is the author, John is the last saved by value.</span></span>
-   <span data-ttu-id="70e27-112">**PID \_ REVNUMBER** est le nombre de fois que la commande File/Save a été appelée sur ce document.</span><span class="sxs-lookup"><span data-stu-id="70e27-112">**PID\_REVNUMBER** is the number of times the File/Save command has been called on this document.</span></span>
-   <span data-ttu-id="70e27-113">Chacune des valeurs de date/heure doit être stockée au format UTC (Universal Coordinated Time).</span><span class="sxs-lookup"><span data-stu-id="70e27-113">Each of the date/time values must be stored in Universal Coordinated Time (UTC).</span></span>
-   <span data-ttu-id="70e27-114">**PID \_ CREATe \_ DTM** est une propriété en lecture seule ; Cette propriété doit être définie lors de la création d’un document, mais ne doit pas être modifiée par la suite.</span><span class="sxs-lookup"><span data-stu-id="70e27-114">**PID\_CREATE\_DTM** is a read-only property; this property should be set when a document is created, but should not be subsequently changed.</span></span>
-   <span data-ttu-id="70e27-115">Pour **la \_ miniature PID**, les applications doivent stocker des données au format **CF \_ DIB** ou **CF \_ MetaFilePict** .</span><span class="sxs-lookup"><span data-stu-id="70e27-115">For **PID\_THUMBNAIL**, applications should store data in **CF\_DIB** or **CF\_METAFILEPICT** format.</span></span> <span data-ttu-id="70e27-116">**CF \_ METAFILEPICT** est recommandé.</span><span class="sxs-lookup"><span data-stu-id="70e27-116">**CF\_METAFILEPICT** is recommended.</span></span>
-   <span data-ttu-id="70e27-117">**PID \_ La sécurité** est le niveau de sécurité suggéré pour le document.</span><span class="sxs-lookup"><span data-stu-id="70e27-117">**PID\_SECURITY** is the suggested security level for the document.</span></span> <span data-ttu-id="70e27-118">En notant le niveau de sécurité du document, une application autre que l’expéditeur du document peut adapter son interface utilisateur aux propriétés.</span><span class="sxs-lookup"><span data-stu-id="70e27-118">By noting the security level on the document, an application other than the originator of the document can adjust its user interface to the properties.</span></span> <span data-ttu-id="70e27-119">Une application ne doit pas afficher d’informations sur un document protégé par mot de passe ou permettre des modifications à des documents Read-Only ou verrouillés pour les annotations.</span><span class="sxs-lookup"><span data-stu-id="70e27-119">An application should not display any information about a password-protected document or enable modifications to enforced Read-Only or Locked-for-Annotations documents.</span></span> <span data-ttu-id="70e27-120">Si l’utilisateur tente de modifier des propriétés, l’application doit avertir l’utilisateur de la Read-Only État recommandé.</span><span class="sxs-lookup"><span data-stu-id="70e27-120">If the user attempts to modify properties, the application should warn the user about the Read-Only Recommended status.</span></span>



| <span data-ttu-id="70e27-121">Niveau de sécurité</span><span class="sxs-lookup"><span data-stu-id="70e27-121">Security level</span></span>         | <span data-ttu-id="70e27-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="70e27-122">Value</span></span> |
|------------------------|-------|
| <span data-ttu-id="70e27-123">Aucune</span><span class="sxs-lookup"><span data-stu-id="70e27-123">None</span></span>                   | <span data-ttu-id="70e27-124">0</span><span class="sxs-lookup"><span data-stu-id="70e27-124">0</span></span>     |
| <span data-ttu-id="70e27-125">Protégé par mot de passe</span><span class="sxs-lookup"><span data-stu-id="70e27-125">Password protected</span></span>     | <span data-ttu-id="70e27-126">1</span><span class="sxs-lookup"><span data-stu-id="70e27-126">1</span></span>     |
| <span data-ttu-id="70e27-127">Lecture seule recommandée</span><span class="sxs-lookup"><span data-stu-id="70e27-127">Read-only recommended</span></span>  | <span data-ttu-id="70e27-128">2</span><span class="sxs-lookup"><span data-stu-id="70e27-128">2</span></span>     |
| <span data-ttu-id="70e27-129">En lecture seule forcé</span><span class="sxs-lookup"><span data-stu-id="70e27-129">Read-only enforced</span></span>     | <span data-ttu-id="70e27-130">4</span><span class="sxs-lookup"><span data-stu-id="70e27-130">4</span></span>     |
| <span data-ttu-id="70e27-131">Verrouillé pour les annotations</span><span class="sxs-lookup"><span data-stu-id="70e27-131">Locked for annotations</span></span> | <span data-ttu-id="70e27-132">8</span><span class="sxs-lookup"><span data-stu-id="70e27-132">8</span></span>     |



 

 

 




