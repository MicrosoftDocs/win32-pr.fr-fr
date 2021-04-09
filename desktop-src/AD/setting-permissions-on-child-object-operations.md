---
title: Définition des autorisations sur les opérations sur les objets enfants
description: Les autorisations, telles que créer un enfant et supprimer un enfant, peuvent également être accordées ou refusées pour des opérations sur tous les sous-objets ou sous-objets d’une classe spécifique.
ms.assetid: fe2f8939-7562-4c03-a7a9-3ac5fc3e81bb
ms.tgt_platform: multiple
keywords:
- Définition des autorisations sur les opérations sur les objets enfants AD
- objets AD, Child, définition d’autorisations sur les opérations d’objets enfants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d407e9b0db865c5df8d5dab53bd97f9f1afa1497
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101420"
---
# <a name="setting-permissions-on-child-object-operations"></a><span data-ttu-id="0cd9c-105">Définition des autorisations sur les opérations sur les objets enfants</span><span class="sxs-lookup"><span data-stu-id="0cd9c-105">Setting Permissions on Child Object Operations</span></span>

<span data-ttu-id="0cd9c-106">Les autorisations, telles que créer un enfant et supprimer un enfant, peuvent également être accordées ou refusées pour des opérations sur tous les sous-objets ou sous-objets d’une classe spécifique.</span><span class="sxs-lookup"><span data-stu-id="0cd9c-106">Permissions, such as Create Child and Delete Child, can also be granted or denied for operations on all subobjects or subobjects of a specific class.</span></span>

<span data-ttu-id="0cd9c-107">La procédure suivante peut être utilisée pour définir des autorisations pour un type de sous-objet spécifique.</span><span class="sxs-lookup"><span data-stu-id="0cd9c-107">The following procedure can be used to set permissions for a specific subobject type.</span></span>

<span data-ttu-id="0cd9c-108">**Pour définir des autorisations pour un type de sous-objet spécifique**</span><span class="sxs-lookup"><span data-stu-id="0cd9c-108">**To set permissions for a specific subobject type**</span></span>

1.  <span data-ttu-id="0cd9c-109">Définissez la propriété [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sur **ADS \_ AceType \_ Access \_ allowed \_ Object** ou **ADS \_ AceType \_ accès \_ refusé \_ Object**.</span><span class="sxs-lookup"><span data-stu-id="0cd9c-109">Set the [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
2.  <span data-ttu-id="0cd9c-110">Définissez la propriété [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sur le GUID de la classe d’objet.</span><span class="sxs-lookup"><span data-stu-id="0cd9c-110">Set the [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to the GUID for object class.</span></span> <span data-ttu-id="0cd9c-111">Il s’agit de la propriété **schemaIDGUID** de l’objet classSchema qui définit la classe d’objets.</span><span class="sxs-lookup"><span data-stu-id="0cd9c-111">This is the **schemaIDGUID** property of the classSchema object that defines the object class.</span></span> <span data-ttu-id="0cd9c-112">Si la propriété **ObjectType** a la **valeur null**, l’entrée du contrôle d’accès s’applique aux sous-objets de n’importe quelle classe.</span><span class="sxs-lookup"><span data-stu-id="0cd9c-112">If the **ObjectType** property is **NULL**, the ACE applies to subobjects of any class.</span></span>
3.  <span data-ttu-id="0cd9c-113">Définissez la propriété [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sur le **type d' \_ objet indicateur ADS \_ \_ \_ présent**.</span><span class="sxs-lookup"><span data-stu-id="0cd9c-113">Set the [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_FLAG\_OBJECT\_TYPE\_PRESENT**.</span></span>

<span data-ttu-id="0cd9c-114">Pour plus d’informations et pour connaître la procédure de création d’une entrée du contrôle d’accès, consultez [définition des droits d’accès sur un objet](setting-access-rights-on-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="0cd9c-114">For more information and a procedure for creating an ACE, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="0cd9c-115">Pour plus d’informations et pour obtenir un exemple de code qui peut être utilisé pour définir une entrée de contrôle d’accès qui contrôle les opérations d’objets enfants, consultez [l’exemple de code pour la définition d’une entrée du contrôle d’accès sur un objet d’annuaire](example-code-for-setting-an-ace-on-a-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="0cd9c-115">For more information and a code example that can be used to set an ACE that controls child object operations, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 