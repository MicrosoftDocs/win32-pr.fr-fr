---
description: Le programme d’installation définit la valeur de la propriété UserSID sur la représentation sous forme de chaîne de l’identificateur de sécurité (SID) de l’utilisateur qui exécute l’installation. Pour plus d’informations, consultez structures d’autorisation.
ms.assetid: 94524636-c7f2-4de2-b35e-644c0c171193
title: UserSID, propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fab01b3f87c654a306bfe3633adf0973ed58aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540486"
---
# <a name="usersid-property"></a><span data-ttu-id="c6242-104">UserSID, propriété</span><span class="sxs-lookup"><span data-stu-id="c6242-104">UserSID property</span></span>

<span data-ttu-id="c6242-105">Le programme d’installation définit la valeur de la propriété **UserSid** sur la représentation sous forme de chaîne de l’identificateur de sécurité (SID) de l’utilisateur qui exécute l’installation.</span><span class="sxs-lookup"><span data-stu-id="c6242-105">The installer sets the value of the **UserSID** property to the string representation of the security identifier (SID) of the user running the installation.</span></span> <span data-ttu-id="c6242-106">Pour plus d’informations, consultez [structures d’autorisation](../secauthz/authorization-structures.md).</span><span class="sxs-lookup"><span data-stu-id="c6242-106">For more information, see [Authorization Structures](../secauthz/authorization-structures.md).</span></span>

## <a name="default-value"></a><span data-ttu-id="c6242-107">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="c6242-107">Default Value</span></span>

<span data-ttu-id="c6242-108">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c6242-108">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6242-109">Notes</span><span class="sxs-lookup"><span data-stu-id="c6242-109">Remarks</span></span>

<span data-ttu-id="c6242-110">La Windows Installer définir cette propriété sur Windows 2000, Windows XP et Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c6242-110">The Windows Installer set this property on Windows 2000, Windows XP and Windows Vista.</span></span> <span data-ttu-id="c6242-111">Cette propriété n’est pas définie sur tous les autres systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="c6242-111">This property is not defined on all other operating systems.</span></span>

<span data-ttu-id="c6242-112">Notez que cette propriété a l’attribut spécial qu’elle peut être récupérée à partir d’une action personnalisée différée.</span><span class="sxs-lookup"><span data-stu-id="c6242-112">Note that this property has the special attribute that it can be retrieved from a deferred custom action.</span></span> <span data-ttu-id="c6242-113">Une action personnalisée exécutée avec des privilèges élevés peut toujours retourner le SID de l’utilisateur dans la propriété **UserSid** .</span><span class="sxs-lookup"><span data-stu-id="c6242-113">A custom action running with elevated privileges can still return the user's SID in **UserSID** property.</span></span> <span data-ttu-id="c6242-114">Pour plus d’informations, consultez [obtention d’informations de contexte pour les actions personnalisées d’exécution différée](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="c6242-114">For information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c6242-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6242-115">Requirements</span></span>



| <span data-ttu-id="c6242-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6242-116">Requirement</span></span> | <span data-ttu-id="c6242-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6242-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6242-118">Version</span><span class="sxs-lookup"><span data-stu-id="c6242-118">Version</span></span><br/> | <span data-ttu-id="c6242-119">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c6242-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c6242-120">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c6242-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c6242-121">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c6242-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c6242-122">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="c6242-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c6242-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6242-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6242-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c6242-124">Properties</span></span>](properties.md)
</dt> </dl>

 

 
