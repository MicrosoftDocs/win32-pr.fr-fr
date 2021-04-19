---
description: Contrôle parental et contrôle de compte d’utilisateur
ms.assetid: dc7c322a-f534-4dda-8c62-aa628a7b91bc
title: Contrôle parental et contrôle de compte d’utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7798661a7cadc4d497791925c83cdfa684b252a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106541208"
---
# <a name="parental-controls-and-user-account-control"></a><span data-ttu-id="5e47c-103">Contrôle parental et contrôle de compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="5e47c-103">Parental Controls and User Account Control</span></span>

<span data-ttu-id="5e47c-104">Le contrôle de compte d’utilisateur (UAC) entraîne la présence de comptes d’utilisateur standard et d’administrateur protégé.</span><span class="sxs-lookup"><span data-stu-id="5e47c-104">User Account Control (UAC) will result in presence of Protected Administrator and Standard User accounts.</span></span> <span data-ttu-id="5e47c-105">Un administrateur protégé s’exécute avec les mêmes droits qu’un utilisateur standard dans le cadre d’une utilisation normale.</span><span class="sxs-lookup"><span data-stu-id="5e47c-105">A Protected Administrator will run with the same rights as a Standard User under normal usage.</span></span> <span data-ttu-id="5e47c-106">Pour les opérations privilégiées :</span><span class="sxs-lookup"><span data-stu-id="5e47c-106">For privileged operations:</span></span>

-   <span data-ttu-id="5e47c-107">Un utilisateur standard affiche la boîte de dialogue informations d’identification de l’interface utilisateur, qui requiert l’entrée d’un nom d’utilisateur et d’un mot de passe pour un administrateur protégé ou un administrateur intégré.</span><span class="sxs-lookup"><span data-stu-id="5e47c-107">A Standard User will be shown the Credentials User Interface dialog box, which requires the input of a user name and password for a Protected Administrator or built-in Administrator.</span></span>
-   <span data-ttu-id="5e47c-108">Un administrateur protégé s’affichera dans la boîte de dialogue de l’interface utilisateur de consentement, ce qui nécessite de sélectionner autoriser pour continuer.</span><span class="sxs-lookup"><span data-stu-id="5e47c-108">A Protected Administrator will be shown the Consent User Interface dialog box, which requires selection of Allow to proceed.</span></span>

<span data-ttu-id="5e47c-109">Il est important de noter que le contrôle de compte d’utilisateur est implémenté par processus, ce qui signifie qu’un processus s’exécute avec élévation de privilèges ou non.</span><span class="sxs-lookup"><span data-stu-id="5e47c-109">It is important to note that UAC is implemented on a per-process basis, so a process either runs elevated or not.</span></span> <span data-ttu-id="5e47c-110">En règle générale, il ne convient pas du point de vue de la sécurité pour exécuter des applications volumineuses comme toujours élevés.</span><span class="sxs-lookup"><span data-stu-id="5e47c-110">Generally, it is not suitable from a security standpoint to run large applications as always elevated.</span></span> <span data-ttu-id="5e47c-111">Pour les contrôles de contrôle parental, le code qui doit modifier les paramètres doit être isolé par l’une des deux options d’implémentation :</span><span class="sxs-lookup"><span data-stu-id="5e47c-111">For Parental Controls, code that must modify settings should be isolated by one of two implementation options:</span></span>

1.  <span data-ttu-id="5e47c-112">Créez un petit exécutable pour la gestion des paramètres qui est marqué dans son manifeste comme nécessitant des droits d’administration.</span><span class="sxs-lookup"><span data-stu-id="5e47c-112">Create a small executable for settings management that is marked in its manifest as requiring administrative rights.</span></span> <span data-ttu-id="5e47c-113">L’appel de l’exécutable entraîne l’affichage de l’interface utilisateur de consentement ou d’informations d’identification avant d’autoriser l’exécution du processus.</span><span class="sxs-lookup"><span data-stu-id="5e47c-113">Invocation of the executable will cause the Consent or Credentials UI to be shown prior to allowing the process to run.</span></span>
2.  <span data-ttu-id="5e47c-114">Fournissez des interfaces COM dans une DLL de produit qui autorisent l’appel par documentation UAC.</span><span class="sxs-lookup"><span data-stu-id="5e47c-114">Provide COM interfaces in a product DLL that allow for invocation per UAC documentation.</span></span> <span data-ttu-id="5e47c-115">Cela entraînera également l’affichage de l’interface utilisateur de consentement ou d’informations d’identification appropriée.</span><span class="sxs-lookup"><span data-stu-id="5e47c-115">This will also cause the appropriate Consent or Credentials UI to be shown.</span></span>

 

 



