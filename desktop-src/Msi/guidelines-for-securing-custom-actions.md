---
description: Pour aider à maintenir une installation logicielle sécurisée, respectez ces instructions lors de la création d’une action personnalisée Windows Installer.
ms.assetid: f7081b0c-bfa2-47a1-840b-28881ad97071
title: Instructions pour la sécurisation des actions personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 119c045833b165222756702244cf65bb2225a8f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203587"
---
# <a name="guidelines-for-securing-custom-actions"></a><span data-ttu-id="982a8-103">Instructions pour la sécurisation des actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="982a8-103">Guidelines for Securing Custom Actions</span></span>

<span data-ttu-id="982a8-104">Le respect des indications suivantes lors de la création d’un package de Windows Installer avec des actions personnalisées vous aide à maintenir un environnement sécurisé lors de l’installation :</span><span class="sxs-lookup"><span data-stu-id="982a8-104">Adherence to the following guidelines when authoring a Windows Installer package with custom actions helps maintain a secure environment during installation:</span></span>

-   <span data-ttu-id="982a8-105">Sécurisez tous les fichiers supplémentaires écrits par votre action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="982a8-105">Secure any additional files written by your custom action.</span></span>
-   <span data-ttu-id="982a8-106">Vérifiez les longueurs de mémoire tampon et la validité de toutes les données lues par votre action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="982a8-106">Check buffer lengths and validity of all data read by your custom action.</span></span> <span data-ttu-id="982a8-107">Cela comprend des propriétés qui peuvent fournir des données à votre action personnalisée, en particulier celles qui utilisent des propriétés publiques fournies par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="982a8-107">This includes properties that may supply data to your custom action, particularly those that use public properties provided by a user.</span></span>
-   <span data-ttu-id="982a8-108">Ne vous fiez pas aux dll externes qui ne sont pas approuvées par le système sur toutes les plateformes sur lesquelles votre package d’installation est destiné à être exécuté.</span><span class="sxs-lookup"><span data-stu-id="982a8-108">Do not rely on external DLLs that are not trusted by the system on all platforms on which your installation package is intended to run.</span></span>
-   <span data-ttu-id="982a8-109">Déterminez avec soin s’il faut utiliser des actions personnalisées qui utilisent des privilèges [*élevés*](e-gly.md) ou l’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="982a8-109">Carefully consider whether to use custom actions that use [*elevated*](e-gly.md) privileges or impersonation.</span></span> <span data-ttu-id="982a8-110">Les actions personnalisées telles que « ouvrir une URL une fois l’installation terminée », « lancer le logiciel une fois l’installation terminée » ou « lancer le fichier Lisez-moi une fois l’installation terminée » ne nécessitent généralement pas de privilèges élevés pour fonctionner.</span><span class="sxs-lookup"><span data-stu-id="982a8-110">Custom actions such as “open a URL after installation is completed,” “launch the software after installation is complete,” or “launch ReadMe after installation is complete” would not usually require elevated privileges to function.</span></span> <span data-ttu-id="982a8-111">Si votre action personnalisée doit s’exécuter avec des privilèges *élevés* , assurez-vous que le code d’action personnalisé protège contre les dépassements de mémoire tampon et le chargement par inadvertance de code non sécurisé.</span><span class="sxs-lookup"><span data-stu-id="982a8-111">If your custom action must run with *elevated* privileges, be sure that the custom action code guards against buffer overruns and inadvertent loading of unsafe code.</span></span> <span data-ttu-id="982a8-112">Notez que pendant la phase d’exécution de l’installation, le programme d’installation transmet les informations à un processus avec des privilèges *élevés* et exécute le script.</span><span class="sxs-lookup"><span data-stu-id="982a8-112">Note that during the execution phase of the installation, the installer passes information to a process with *elevated* privileges and runs the script.</span></span> <span data-ttu-id="982a8-113">Toutes les actions personnalisées qui s’exécutent pendant la phase d’exécution peuvent s’exécuter avec des privilèges *élevés* .</span><span class="sxs-lookup"><span data-stu-id="982a8-113">Any custom actions that run during the execution phase may run with *elevated* privileges.</span></span>
-   <span data-ttu-id="982a8-114">Rassemblez toutes les informations fournies par l’utilisateur pendant la séquence d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="982a8-114">Gather all information provided by the user during the UI sequence.</span></span> <span data-ttu-id="982a8-115">Ne pas inviter l’utilisateur à fournir des informations qui ne peuvent pas être définies à l’aide d’une propriété publique.</span><span class="sxs-lookup"><span data-stu-id="982a8-115">Do not prompt the user for any information that can't be set using a public property.</span></span>
-   <span data-ttu-id="982a8-116">Si votre action personnalisée de script développe des propriétés, prenez des précautions que l’action personnalisée est sécurisée par rapport à la possibilité d’injection de script.</span><span class="sxs-lookup"><span data-stu-id="982a8-116">If your script custom action expands properties, take precautions that the custom action is secured against the possibility of script injection.</span></span> <span data-ttu-id="982a8-117">Le script peut être enregistré en texte clair.</span><span class="sxs-lookup"><span data-stu-id="982a8-117">Script may be logged in clear text.</span></span>

<span data-ttu-id="982a8-118">Voir aussi [sécurité des actions personnalisées](custom-action-security.md).</span><span class="sxs-lookup"><span data-stu-id="982a8-118">See also [Custom Action Security](custom-action-security.md).</span></span>

 

 



