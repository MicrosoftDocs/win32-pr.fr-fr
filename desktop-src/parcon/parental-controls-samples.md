---
description: Exemples de contrôle parental
ms.assetid: 19dac95c-2279-4bf9-a58c-dd30177c0c9d
title: Exemples de contrôle parental
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26962f4edd16e1e860883607316d5a7cbf3d9122
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534690"
---
# <a name="parental-controls-samples"></a><span data-ttu-id="58857-103">Exemples de contrôle parental</span><span class="sxs-lookup"><span data-stu-id="58857-103">Parental Controls Samples</span></span>

<span data-ttu-id="58857-104">Des exemples de code pour les contrôles parentaux sont disponibles sous chemins d’accès <installation directory> \\ Windows \\ <version number> \\ exemples de \\ sécurité \\ parentalcontrols.</span><span class="sxs-lookup"><span data-stu-id="58857-104">Sample code for Parental Controls is available under path <installation directory>\\Windows\\<version number>\\Samples\\Security\\ParentalControls.</span></span> <span data-ttu-id="58857-105">Les exemples sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="58857-105">The samples are as follows:</span></span>

## <a name="utilities"></a><span data-ttu-id="58857-106">Services</span><span class="sxs-lookup"><span data-stu-id="58857-106">Utilities</span></span>

<span data-ttu-id="58857-107">Fonctionnalités d’assistance pour la gestion COM de base, les opérations de chaîne SID et les fonctionnalités de lecture et d’écriture WMI.</span><span class="sxs-lookup"><span data-stu-id="58857-107">Helper functionality for basic COM management, SID string operations, and WMI read and write functionality.</span></span> <span data-ttu-id="58857-108">Tous les autres exemples dépendent de ce projet, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="58857-108">All of the other samples depend on this project unless otherwise specified.</span></span>

## <a name="complianceapi"></a><span data-ttu-id="58857-109">ComplianceAPI</span><span class="sxs-lookup"><span data-stu-id="58857-109">ComplianceAPI</span></span>

<span data-ttu-id="58857-110">Application console pilotée par ligne de commande montrant comment utiliser l’API de compatibilité pour récupérer un sous-ensemble de paramètres de clé pour un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="58857-110">Command-line driven console application demonstrating how to use the Compliance API to retrieve a key subset of settings for a user.</span></span>

## <a name="complianceapp"></a><span data-ttu-id="58857-111">ComplianceApp</span><span class="sxs-lookup"><span data-stu-id="58857-111">ComplianceApp</span></span>

<span data-ttu-id="58857-112">Application console simple illustrant l’utilisation de l’API de conformité pour vérifier la journalisation requise et les restrictions spécifiques.</span><span class="sxs-lookup"><span data-stu-id="58857-112">Simple console application demonstrating use of the Compliance API to check for logging required and specific restrictions.</span></span> <span data-ttu-id="58857-113">Si les restrictions de temps sont activées, l’application attend également les événements de déconnexion imminents.</span><span class="sxs-lookup"><span data-stu-id="58857-113">If time restrictions are enabled, the application also waits for the impending logout events.</span></span>

## <a name="uiextensibility"></a><span data-ttu-id="58857-114">UIExtensibility</span><span class="sxs-lookup"><span data-stu-id="58857-114">UIExtensibility</span></span>

<span data-ttu-id="58857-115">Application console pilotée par ligne de commande illustrant l’utilisation des API WMI et du schéma WPC pour répertorier, interroger, ajouter, modifier et supprimer des entrées de lien d’extensibilité de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="58857-115">Command-line driven console application demonstrating use of the WMI APIs and WPC schema to list, query, add, modify, and delete UI Extensibility link entries.</span></span>

<span data-ttu-id="58857-116">Exemple de ligne de commande pour l’exemple :</span><span class="sxs-lookup"><span data-stu-id="58857-116">Example command line for sample:</span></span>

<span data-ttu-id="58857-117">"D : \\ WPC \\ Samples \\ Security \\ parentalcontrols \\ UIExtensibility \\ Debug \\ UIExtensibility" Add/g : {FD59BB7F-54AB-11DB-9666-00E08161165F}/c : 0/N : D:/WPC/Samples/Security/parentalcontrols/UiExtRC/Debug/UiExtRC.dll,-101/S : D:/WPC/Samples/Security/parentalcontrols/UiExtRC/Debug/UiExtRC.dll,-103/I : d:/WPC/Samples/Security/parentalcontrols/UiExtRC/Debug/UiExtRC.dll,-104/D : d:/WPC/Samples/Security/parentalcontrols/UiExtRC/Debug/UiExtRC.dll,-106/e : c : \\ Windows \\Notepad.exe</span><span class="sxs-lookup"><span data-stu-id="58857-117">"D:\\WPC\\Samples\\Security\\ParentalControls\\UIExtensibility\\debug\\UIExtensibility" add /g:{FD59BB7F-54AB-11DB-9666-00E08161165F} /c:0 /n:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-101 /s:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-103 /i:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-104 /d:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-106 /e:c:\\windows\\Notepad.exe</span></span>

<span data-ttu-id="58857-118">où UiExtRC est une DLL de ressource simple avec des ressources de chaîne pour les ID 101 et 103, et 24x24 pixel 32 bits avec des bitmaps alpha pour les ressources 104 et 106.</span><span class="sxs-lookup"><span data-stu-id="58857-118">where UiExtRC is a simple resource DLL with string resources for ID's 101 and 103, and 24x24 pixel 32-bit with alpha bitmaps for resources 104 and 106.</span></span>

## <a name="webextensibility"></a><span data-ttu-id="58857-119">Extensibilité</span><span class="sxs-lookup"><span data-stu-id="58857-119">WebExtensibility</span></span>

<span data-ttu-id="58857-120">Application console pilotée par ligne de commande montrant comment utiliser les API WMI et le schéma WPC pour répertorier, ajouter et supprimer des entrées d’exemption d’URL ou d’application HTTP, et pour définir et réinitialiser un remplacement de filtre de contenu Web avec les propriétés FilterID et FilterName.</span><span class="sxs-lookup"><span data-stu-id="58857-120">Command-line driven console application demonstrating how to use the WMI APIs and WPC schema to list, add, and delete HTTP application or URL exemption entries, and to set and reset a Web Content Filter override with the FilterID and FilterName properties.</span></span>

<span data-ttu-id="58857-121">L’accès aux listes d’exemptions d’URL et d’applications HTTP en lecture seule n’est pas affiché, mais le code permettant de lire les listes est le même que pour le cas de lecture/écriture, à l’exception de la modification du paramètre WMI.</span><span class="sxs-lookup"><span data-stu-id="58857-121">Access to the read-only HTTP application and URL exemption lists is not shown, but the code to read the lists would be the same as for the read/write case except for modification of the WMI parameter.</span></span>

 

 



