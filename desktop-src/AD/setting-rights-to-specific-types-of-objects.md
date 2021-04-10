---
title: Définition de droits sur des types d’objets spécifiques
description: La procédure suivante montre comment définir une entrée du contrôle d’accès qui peut être héritée uniquement par une classe d’objets spécifique.
ms.assetid: 42712458-69c7-4fe1-bfb3-b3fb28092a56
ms.tgt_platform: multiple
keywords:
- définition de droits sur les types d’objets AD
- objets AD, définition de droits sur
- Active Directory, utilisation de, sécurité, définition de droits sur des types d’objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f44cfbe753e6f92787f8269eab1f4eab4c2e98
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103940794"
---
# <a name="setting-rights-to-specific-types-of-objects"></a><span data-ttu-id="20601-106">Définition de droits sur des types d’objets spécifiques</span><span class="sxs-lookup"><span data-stu-id="20601-106">Setting Rights to Specific Types of Objects</span></span>

<span data-ttu-id="20601-107">La procédure suivante montre comment définir une entrée du contrôle d’accès qui peut être héritée uniquement par une classe d’objets spécifique.</span><span class="sxs-lookup"><span data-stu-id="20601-107">The following procedure shows how to set an ACE that can be inherited only by a specific class of objects.</span></span>

 <span data-ttu-id="20601-108">**Pour définir une entrée du contrôle d’accès qui peut être héritée uniquement par une classe d’objets spécifique**</span><span class="sxs-lookup"><span data-stu-id="20601-108">**To set an ACE that can be inherited only by a specific class of objects**</span></span>

1.  <span data-ttu-id="20601-109">Définissez la propriété [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sur **ADS \_ AceType \_ Access \_ allowed \_ Object** ou **ADS \_ AceType \_ accès \_ refusé \_ Object**.</span><span class="sxs-lookup"><span data-stu-id="20601-109">Set the [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
2.  <span data-ttu-id="20601-110">Définissez la propriété [**IADsAccessControlEntry. AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) de façon à inclure \_ l' \_ indicateur ACE inherit ACEFLAG de publicités \_ .</span><span class="sxs-lookup"><span data-stu-id="20601-110">Set the [**IADsAccessControlEntry.AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to include the ADS\_ACEFLAG\_INHERIT\_ACE flag.</span></span>
3.  <span data-ttu-id="20601-111">Définissez la propriété [**IADsAccessControlEntry. InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sur le **schemaIDGUID** de la classe d’objet qui peut hériter de l’entrée du contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="20601-111">Set the [**IADsAccessControlEntry.InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to the **schemaIDGUID** of the object class that can inherit the ACE.</span></span>
4.  <span data-ttu-id="20601-112">Définissez la propriété [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sur le **type d' \_ objet hérité d’indicateur ADS \_ \_ \_ présent**.</span><span class="sxs-lookup"><span data-stu-id="20601-112">Set the [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_FLAG\_INHERITED OBJECT\_TYPE\_PRESENT**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="20601-113">Définissez **ad \_ ACEFLAG \_ inherit \_ ACE** pour que l’entrée du contrôle d’accès soit héritée.</span><span class="sxs-lookup"><span data-stu-id="20601-113">Set **ADS\_ACEFLAG\_INHERIT\_ACE** to cause the ACE to be inherited.</span></span> <span data-ttu-id="20601-114">En outre, vous devez définir les **publicités \_ ACEFLAG hériter de l' \_ \_ \_ ACE uniquement** si le type d’objet auquel s’applique cette entrée du contrôle d’accès ne correspond pas au type d’objet du conteneur dans lequel l’entrée du contrôle d’accès est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="20601-114">In addition, you must set **ADS\_ACEFLAG\_INHERIT\_ONLY\_ACE** if the object type this ACE applies to does not match the object type of the container where the ACE is specified.</span></span> <span data-ttu-id="20601-115">Si ce n’est pas le cas, l’entrée du contrôle d’accès prendra également effet sur le conteneur et peut accorder des droits inattendus.</span><span class="sxs-lookup"><span data-stu-id="20601-115">If this is not done, the ACE will also become effective on the container and can grant unintended rights.</span></span>

 

<span data-ttu-id="20601-116">Pour plus d’informations et d’exemples de code qui peuvent être utilisés pour définir ce type d’entrée du contrôle d’accès, consultez [exemple de code pour la définition d’une entrée](example-code-for-setting-an-ace-on-a-directory-object.md)du contrôle d’accès sur un objet d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="20601-116">For more information and code examples that can be used to set this type of ACE, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 