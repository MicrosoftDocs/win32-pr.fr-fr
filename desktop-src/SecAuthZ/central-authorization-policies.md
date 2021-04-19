---
description: Une stratégie d’autorisation centrale collecte les règles d’autorisation spécifiques (CAPRs) dans une seule stratégie.
ms.assetid: E3E43D9F-6826-468A-86E9-AC8F9A381FD4
title: Stratégies d’autorisation centralisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b890236b0dae0f8f8d51254def4e1607cc35894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529716"
---
# <a name="central-authorization-policies"></a><span data-ttu-id="9ed37-103">Stratégies d’autorisation centralisées</span><span class="sxs-lookup"><span data-stu-id="9ed37-103">Central Authorization Policies</span></span>

<span data-ttu-id="9ed37-104">Une stratégie d’autorisation centrale collecte les règles d’autorisation spécifiques (CAPRs) dans une seule stratégie.</span><span class="sxs-lookup"><span data-stu-id="9ed37-104">A Central Authorization Policy (CAP) collects the specific authorization rules (CAPRs) into a single policy.</span></span> <span data-ttu-id="9ed37-105">Pour permettre la combinaison des règles d’autorisation spécifiques dans la stratégie d’autorisation holistique de l’organisation, CAPRs peut être référencé et appliqué à un ensemble de ressources.</span><span class="sxs-lookup"><span data-stu-id="9ed37-105">To allow the specific authorization rules (CAPRs) to be combined into the holistic authorization policy of the organization, CAPRs can be referenced together and applied to a set of resources.</span></span> <span data-ttu-id="9ed37-106">Pour ce faire, il faut collecter plusieurs (par référence) dans un capuchon.</span><span class="sxs-lookup"><span data-stu-id="9ed37-106">This is done by collecting multiple (by reference) into a CAP.</span></span> <span data-ttu-id="9ed37-107">Une fois qu’une limite est définie, elle peut être distribuée consommée par les gestionnaires de ressources pour appliquer la stratégie d’autorisation des organisations aux ressources.</span><span class="sxs-lookup"><span data-stu-id="9ed37-107">Once a CAP is defined it can be distributed consumed by resource managers to apply the organizations authorization policy to resources.</span></span>

<span data-ttu-id="9ed37-108">Un CAP a les attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="9ed37-108">A CAP has the following attributes:</span></span>

-   <span data-ttu-id="9ed37-109">Collection de CAPRs : liste de références aux objets CAPR existants</span><span class="sxs-lookup"><span data-stu-id="9ed37-109">Collection of CAPRs – a list of references to existing CAPR objects</span></span>
-   <span data-ttu-id="9ed37-110">Identificateur (SID)</span><span class="sxs-lookup"><span data-stu-id="9ed37-110">An identifier (Sid)</span></span>
-   <span data-ttu-id="9ed37-111">Description</span><span class="sxs-lookup"><span data-stu-id="9ed37-111">Description</span></span>
-   <span data-ttu-id="9ed37-112">Nom</span><span class="sxs-lookup"><span data-stu-id="9ed37-112">Name</span></span>

<span data-ttu-id="9ed37-113">Un capuchon est évalué lors de l’évaluation de l’accès pour les fichiers et dossiers sur lesquels un administrateur l’active.</span><span class="sxs-lookup"><span data-stu-id="9ed37-113">A CAP is evaluated during access evaluation for files and folders on which an administrator enables it.</span></span> <span data-ttu-id="9ed37-114">Lors d’un appel [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) , la vérification de la limite est logiquement associée à la vérification de la liste de contrôle d’accès discrétionnaire. Cela signifie que pour obtenir l’accès à un fichier auquel l’extrémité s’applique, un utilisateur doit avoir accès à la fois en fonction de l’extrémité (son CAPRs associé) et à la liste de contrôle d’accès discrétionnaire sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="9ed37-114">During an [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) call, the CAP check is logically combined with the discretionary ACL check; this means that in order to obtain access to a file to which the CAP applies, a user needs to have access both according to the CAP (its associated CAPRs) and the discretionary ACL on the file.</span></span>

<span data-ttu-id="9ed37-115">Exemple d’extrémité :</span><span class="sxs-lookup"><span data-stu-id="9ed37-115">Example CAP:</span></span>

``` syntax
CORPORATE-FINANCE-CAP]
CAPID=S-1-5-3-4-56-45-67-123
Policies=HBI-CAPE;RETENTION-CAPR
```

## <a name="cap-definition"></a><span data-ttu-id="9ed37-116">Définition de l’extrémité</span><span class="sxs-lookup"><span data-stu-id="9ed37-116">CAP Definition</span></span>

<span data-ttu-id="9ed37-117">Un capuchon est créé et modifié dans Active Directory à l’aide d’une nouvelle expérience utilisateur dans le Centre (ou PowerShell) qui permet à l’administrateur de créer un capuchon et de spécifier un ensemble de CAPRs qui composent l’extrémité.</span><span class="sxs-lookup"><span data-stu-id="9ed37-117">A CAP is created and edited in Active Directory using a new UX in ADAC (or PowerShell) that allows the administrator to create a CAP and specify a set of CAPRs that make up the CAP.</span></span>

 

 
