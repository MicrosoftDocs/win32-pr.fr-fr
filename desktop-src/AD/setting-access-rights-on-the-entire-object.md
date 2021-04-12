---
title: Définition des droits d’accès sur l’objet entier
description: Certaines autorisations peuvent être définies uniquement pour un objet entier, par exemple supprimer et répertorier le contenu. Les autorisations spécifiques à l’opération, telles que l’autorisation lecture, peuvent également être définies pour l’ensemble de l’objet afin qu’elles s’appliquent à un objet entier.
ms.assetid: 786357f4-146e-4638-8bd6-82bc1a6640a1
ms.tgt_platform: multiple
keywords:
- Définition des droits d’accès sur l’ensemble de l’objet AD
- objets AD, définition des droits d’accès sur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9a965b646de1ee3eba40757386fd243839cb35b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462818"
---
# <a name="setting-access-rights-on-the-entire-object"></a><span data-ttu-id="0caac-106">Définition des droits d’accès sur l’objet entier</span><span class="sxs-lookup"><span data-stu-id="0caac-106">Setting Access Rights on the Entire Object</span></span>

<span data-ttu-id="0caac-107">Certaines autorisations peuvent être définies uniquement pour un objet entier, par exemple supprimer et répertorier le contenu.</span><span class="sxs-lookup"><span data-stu-id="0caac-107">Certain permissions can be set only for an entire object, such as Delete and List Contents.</span></span> <span data-ttu-id="0caac-108">Les autorisations spécifiques à l’opération, telles que l’autorisation lecture, peuvent également être définies pour l’ensemble de l’objet afin qu’elles s’appliquent à un objet entier.</span><span class="sxs-lookup"><span data-stu-id="0caac-108">Operation-specific permissions, such as the Read permission, can also be set for entire object so that they apply to an entire object.</span></span>

<span data-ttu-id="0caac-109">La procédure suivante peut être utilisée pour définir des autorisations pour un objet entier.</span><span class="sxs-lookup"><span data-stu-id="0caac-109">The following procedure can be used to set permissions for an entire object.</span></span>

<span data-ttu-id="0caac-110">**Pour définir des autorisations pour un objet entier**</span><span class="sxs-lookup"><span data-stu-id="0caac-110">**To set permissions for an entire object**</span></span>

1.  <span data-ttu-id="0caac-111">Définissez [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sur **ADS \_ AceType \_ accès \_ autorisé** ou **ad \_ AceType \_ accès \_ refusé**.</span><span class="sxs-lookup"><span data-stu-id="0caac-111">Set [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_ACETYPE\_ACCESS\_ALLOWED** or **ADS\_ACETYPE\_ACCESS\_DENIED**.</span></span>
2.  <span data-ttu-id="0caac-112">Affectez à [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) et **IADsAccessControlEntry. InheritedObjectType** la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="0caac-112">Set [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) and **IADsAccessControlEntry.InheritedObjectType** to **NULL**.</span></span>

<span data-ttu-id="0caac-113">Pour plus d’informations sur la création d’une entrée du contrôle d’accès, consultez [définition des droits d’accès sur un objet](setting-access-rights-on-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="0caac-113">For more information about how to create an ACE, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="0caac-114">Pour plus d’informations et pour obtenir un exemple de code qui peut être utilisé pour définir une entrée du contrôle d’accès, consultez [exemple de code pour la définition d’une entrée du contrôle d’accès sur un objet d’annuaire](example-code-for-setting-an-ace-on-a-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="0caac-114">For more information and a code example that can be used to set an ACE, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 