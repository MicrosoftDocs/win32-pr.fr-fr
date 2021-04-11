---
description: Répertorie les interfaces dans les API d’authentification.
ms.assetid: bde3bcae-2152-4589-92a0-b44d98f233ef
title: Interfaces d’authentification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b101fd4fdd3c518d24b5b6f798fcaa4e0327dd22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203382"
---
# <a name="authentication-interfaces"></a><span data-ttu-id="6943c-103">Interfaces d’authentification</span><span class="sxs-lookup"><span data-stu-id="6943c-103">Authentication Interfaces</span></span>

<span data-ttu-id="6943c-104">Les interfaces d’authentification sont classées en fonction de l’utilisation comme suit :</span><span class="sxs-lookup"><span data-stu-id="6943c-104">Authentication interfaces are categorized according to usage as follows:</span></span>

-   [<span data-ttu-id="6943c-105">Interfaces de carte à puce</span><span class="sxs-lookup"><span data-stu-id="6943c-105">Smart Card Interfaces</span></span>](#smart-card-interfaces)
-   [<span data-ttu-id="6943c-106">Interfaces de partage d’identité</span><span class="sxs-lookup"><span data-stu-id="6943c-106">Identity Sharing Interfaces</span></span>](#identity-sharing-interfaces)

## <a name="smart-card-interfaces"></a><span data-ttu-id="6943c-107">Interfaces de carte à puce</span><span class="sxs-lookup"><span data-stu-id="6943c-107">Smart Card Interfaces</span></span>

<span data-ttu-id="6943c-108">Le kit de développement logiciel (SDK) de carte à puce fournit les interfaces COM suivantes.</span><span class="sxs-lookup"><span data-stu-id="6943c-108">The Smart Card SDK provides the following COM interfaces.</span></span> <span data-ttu-id="6943c-109">Les méthodes pour une interface spécifique sont répertoriées dans la table des matières et dans la page de référence de cette interface.</span><span class="sxs-lookup"><span data-stu-id="6943c-109">The methods for a specific interface are listed in the Table of Contents and on the reference page for that interface.</span></span>



| <span data-ttu-id="6943c-110">Interface</span><span class="sxs-lookup"><span data-stu-id="6943c-110">Interface</span></span>                                    | <span data-ttu-id="6943c-111">Description</span><span class="sxs-lookup"><span data-stu-id="6943c-111">Description</span></span>                                                                                                                                                                              |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6943c-112">**IByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="6943c-112">**IByteBuffer**</span></span>](ibytebuffer.md)           | <span data-ttu-id="6943c-113">Gère un objet de flux.</span><span class="sxs-lookup"><span data-stu-id="6943c-113">Manages a stream object.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="6943c-114">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="6943c-114">**ISCard**</span></span>](iscard.md)                     | <span data-ttu-id="6943c-115">Ouvre et gère une connexion à une [*carte à puce*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="6943c-115">Opens and manages a connection to a [*smart card*](/windows/desktop/SecGloss/s-gly).</span></span>                                                                    |
| [<span data-ttu-id="6943c-116">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="6943c-116">**ISCardAuth**</span></span>](iscardauth.md)             | <span data-ttu-id="6943c-117">Authentifie une application, une carte à puce ou un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6943c-117">Authenticates an application, smart card, or user.</span></span>                                                                                                                                       |
| [<span data-ttu-id="6943c-118">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="6943c-118">**ISCardCmd**</span></span>](iscardcmd.md)               | <span data-ttu-id="6943c-119">Construit et gère une [*unité de données de protocole d’application*](/windows/desktop/SecGloss/a-gly) de carte à puce (APDU).</span><span class="sxs-lookup"><span data-stu-id="6943c-119">Constructs and manages a smart card [*Application Protocol Data Unit*](/windows/desktop/SecGloss/a-gly) (APDU).</span></span> |
| [<span data-ttu-id="6943c-120">**ISCardDatabase**</span><span class="sxs-lookup"><span data-stu-id="6943c-120">**ISCardDatabase**</span></span>](iscarddatabase.md)     | <span data-ttu-id="6943c-121">Effectue les opérations de base de données du [*Gestionnaire de ressources*](/windows/desktop/SecGloss/r-gly) de carte à puce.</span><span class="sxs-lookup"><span data-stu-id="6943c-121">Performs smart card [*resource manager*](/windows/desktop/SecGloss/r-gly) database operations.</span></span>                                              |
| [<span data-ttu-id="6943c-122">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="6943c-122">**ISCardFileAccess**</span></span>](iscardfileaccess.md) | <span data-ttu-id="6943c-123">Exécute des services de fichiers communs tels que la localisation, la sélection, la lecture, l’écriture, la création et la suppression de fichiers.</span><span class="sxs-lookup"><span data-stu-id="6943c-123">Performs common file services such as locating, selecting, reading, writing, creating, and deleting files.</span></span>                                                                               |
| [<span data-ttu-id="6943c-124">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="6943c-124">**ISCardISO7816**</span></span>](iscardiso7816.md)       | <span data-ttu-id="6943c-125">Construit une commande APDU.</span><span class="sxs-lookup"><span data-stu-id="6943c-125">Constructs an APDU command.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="6943c-126">**ISCardLocate**</span><span class="sxs-lookup"><span data-stu-id="6943c-126">**ISCardLocate**</span></span>](iscardlocate.md)         | <span data-ttu-id="6943c-127">Localise une carte à puce.</span><span class="sxs-lookup"><span data-stu-id="6943c-127">Locates a smart card.</span></span>                                                                                                                                                                    |
| [<span data-ttu-id="6943c-128">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="6943c-128">**ISCardManage**</span></span>](iscardmanage.md)         | <span data-ttu-id="6943c-129">Gère le système de carte à puce.</span><span class="sxs-lookup"><span data-stu-id="6943c-129">Manages the smart card system.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="6943c-130">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="6943c-130">**ISCardTypeConv**</span></span>](iscardtypeconv.md)     | <span data-ttu-id="6943c-131">Fournit des méthodes utilisées pour prendre en charge d’autres interfaces COM de carte à puce.</span><span class="sxs-lookup"><span data-stu-id="6943c-131">Provides methods used to support other smart card COM interfaces.</span></span> <span data-ttu-id="6943c-132">Cette interface n’est fournie qu’à des fins de compatibilité descendante et ne doit plus être utilisée.</span><span class="sxs-lookup"><span data-stu-id="6943c-132">This interface is provided for backward compatibility only and should no longer be used.</span></span>                               |
| [<span data-ttu-id="6943c-133">**ISCardVerify**</span><span class="sxs-lookup"><span data-stu-id="6943c-133">**ISCardVerify**</span></span>](iscardverify.md)         | <span data-ttu-id="6943c-134">Vérifie ou modifie la stratégie de vérification des titulaires de cartes (IVT).</span><span class="sxs-lookup"><span data-stu-id="6943c-134">Verifies or changes card holder verification (CHV) policy.</span></span>                                                                                                                               |



 

## <a name="identity-sharing-interfaces"></a><span data-ttu-id="6943c-135">Interfaces de partage d’identité</span><span class="sxs-lookup"><span data-stu-id="6943c-135">Identity Sharing Interfaces</span></span>

<span data-ttu-id="6943c-136">Le kit de développement logiciel (SDK) partage d’identité fournit les interfaces COM suivantes.</span><span class="sxs-lookup"><span data-stu-id="6943c-136">The Identity Sharing SDK provides the following COM interfaces.</span></span> <span data-ttu-id="6943c-137">Les méthodes pour une interface spécifique sont répertoriées dans la table des matières et dans la page de référence de cette interface.</span><span class="sxs-lookup"><span data-stu-id="6943c-137">The methods for a specific interface are listed in the Table of Contents and on the reference page for that interface.</span></span>



| <span data-ttu-id="6943c-138">Interface</span><span class="sxs-lookup"><span data-stu-id="6943c-138">Interface</span></span>                                                          | <span data-ttu-id="6943c-139">Description</span><span class="sxs-lookup"><span data-stu-id="6943c-139">Description</span></span>                                                                              |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6943c-140">**IAssociatedIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="6943c-140">**IAssociatedIdentityProvider**</span></span>](/windows/desktop/api/IdentityProvider/nn-identityprovider-iassociatedidentityprovider) | <span data-ttu-id="6943c-141">Permet à un fournisseur d’identité d’associer des identités à des comptes d’utilisateurs locaux.</span><span class="sxs-lookup"><span data-stu-id="6943c-141">Allows an identity provider to associate identities with local user accounts.</span></span>            |
| [<span data-ttu-id="6943c-142">**IIdentityAdvise**</span><span class="sxs-lookup"><span data-stu-id="6943c-142">**IIdentityAdvise**</span></span>](/windows/desktop/api/IdentityProvider/nn-identityprovider-iidentityadvise)                         | <span data-ttu-id="6943c-143">Permet à un fournisseur d’identité de notifier une application appelante lorsqu’une identité est mise à jour.</span><span class="sxs-lookup"><span data-stu-id="6943c-143">Allows an identity provider to notify a calling application when an identity is updated.</span></span> |
| [<span data-ttu-id="6943c-144">**IIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="6943c-144">**IIdentityProvider**</span></span>](/windows/desktop/api/Identityprovider/nn-identityprovider-iidentityprovider)                     | <span data-ttu-id="6943c-145">Représente un fournisseur d'identité.</span><span class="sxs-lookup"><span data-stu-id="6943c-145">Represents an identity provider.</span></span>                                                         |
| [<span data-ttu-id="6943c-146">**IIdentityStore**</span><span class="sxs-lookup"><span data-stu-id="6943c-146">**IIdentityStore**</span></span>](/windows/desktop/api/Identitystore/nn-identitystore-iidentitystore)                           | <span data-ttu-id="6943c-147">Fournit des méthodes pour énumérer et gérer des identités et des fournisseurs d’identité.</span><span class="sxs-lookup"><span data-stu-id="6943c-147">Provides methods to enumerate and manage identities and identity providers.</span></span>              |



 

 

 
