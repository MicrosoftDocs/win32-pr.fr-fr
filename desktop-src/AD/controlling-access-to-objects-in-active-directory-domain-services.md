---
title: Contrôle de l’accès aux objets dans Active Directory Domain Services
description: Chaque objet de service d’annuaire Active Directory est protégé par la sécurité Windows 2000.
ms.assetid: 0821069d-76bd-49cb-a617-8446d26e61d9
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, utilisation, sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cac744ef63fa95c45d5af535f5155378d479fdb
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/04/2019
ms.locfileid: "104030656"
---
# <a name="controlling-object-access-in-active-directory-domain-services"></a><span data-ttu-id="d3a92-104">Contrôle de l’accès aux objets dans Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="d3a92-104">Controlling object access in Active Directory Domain Services</span></span>

<span data-ttu-id="d3a92-105">Chaque objet de service d’annuaire Active Directory est protégé par la sécurité Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d3a92-105">Each Active Directory directory service object is protected by Windows 2000 security.</span></span> <span data-ttu-id="d3a92-106">Cette protection de sécurité contrôle les opérations que chaque principal de sécurité peut effectuer dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="d3a92-106">This security protection controls the operations that each security principal can perform in the directory.</span></span> <span data-ttu-id="d3a92-107">Les sections suivantes décrivent comment une application activée pour les annuaires peut utiliser les fonctionnalités de contrôle d’accès dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d3a92-107">The following sections describe how a directory-enabled application can use the access control features in Active Directory.</span></span>

-   [<span data-ttu-id="d3a92-108">Fonctionnement de Access Control dans Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="d3a92-108">How Access Control Works in Active Directory Domain Services</span></span>](how-access-control-works-in-active-directory-domain-services.md)
-   [<span data-ttu-id="d3a92-109">Impact du contrôle d’accès sur les opérations de lecture, d’écriture, de création et de suppression d’objets.</span><span class="sxs-lookup"><span data-stu-id="d3a92-109">How access control affects read operations, write operation, object creation and deletion.</span></span>](how-security-affects-operations-in-active-directory-domain-services.md)
-   [<span data-ttu-id="d3a92-110">Utilisation des interfaces IADs et IDirectoryObject pour travailler avec le descripteur de sécurité d’un objet</span><span class="sxs-lookup"><span data-stu-id="d3a92-110">Using the IADs and IDirectoryObject interfaces to work with an object's security descriptor</span></span>](apis-for-working-with-security-descriptors.md)
-   [<span data-ttu-id="d3a92-111">Modification des autorisations d’accès sur un objet</span><span class="sxs-lookup"><span data-stu-id="d3a92-111">Modifying the access permissions on an object</span></span>](setting-access-rights-on-an-object.md)
-   [<span data-ttu-id="d3a92-112">Définition des descripteurs de sécurité sur les nouveaux objets d’annuaire</span><span class="sxs-lookup"><span data-stu-id="d3a92-112">How security descriptors are set on new directory objects</span></span>](how-security-descriptors-are-set-on-new-directory-objects.md)
-   [<span data-ttu-id="d3a92-113">Création d’un descripteur de sécurité pour un nouvel objet d’annuaire</span><span class="sxs-lookup"><span data-stu-id="d3a92-113">Creating a Security Descriptor for a New Directory Object</span></span>](creating-a-security-descriptor-for-a-new-directory-object.md)
-   [<span data-ttu-id="d3a92-114">Utilisation de l’héritage des autorisations d’accès pour permettre l’accès administratif à l’intégralité d’une sous-arborescence du répertoire</span><span class="sxs-lookup"><span data-stu-id="d3a92-114">Using inheritance of access permissions to enable administrative access to an entire subtree of the directory</span></span>](inheritance-and-delegation-of-administration.md)
-   [<span data-ttu-id="d3a92-115">Création, modification et lecture du descripteur de sécurité par défaut pour une classe d’objets</span><span class="sxs-lookup"><span data-stu-id="d3a92-115">Creating, modifying, and reading the default security descriptor for an object class</span></span>](default-security-descriptor.md)
-   [<span data-ttu-id="d3a92-116">Création, définition et vérification des droits d’accès de contrôle pour les opérations qui dépassent celles couvertes par les droits prédéfinis</span><span class="sxs-lookup"><span data-stu-id="d3a92-116">Creating, setting, and checking control access rights for operations that go beyond those covered by the predefined rights</span></span>](control-access-rights.md)
-   [<span data-ttu-id="d3a92-117">Utilisation de DsAddSidHistory</span><span class="sxs-lookup"><span data-stu-id="d3a92-117">Using DsAddSidHistory</span></span>](using-dsaddsidhistory.md)
-   [<span data-ttu-id="d3a92-118">Contrôle de la visibilité des objets</span><span class="sxs-lookup"><span data-stu-id="d3a92-118">Controlling Object Visibility</span></span>](controlling-object-visibility.md)
-   [<span data-ttu-id="d3a92-119">DACL null et DACL vides</span><span class="sxs-lookup"><span data-stu-id="d3a92-119">Null DACLs and Empty DACLs</span></span>](null-dacls-and-empty-dacls.md)

 

 




