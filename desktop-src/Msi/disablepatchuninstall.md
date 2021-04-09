---
description: Si cette stratégie système par ordinateur est définie sur 1, les correctifs ne peuvent pas être supprimés de l’ordinateur par un utilisateur ou un administrateur.
ms.assetid: e964cb2b-ceaa-4122-bf54-cf1eeab4bc25
title: DisablePatchUninstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2de1bc85a249b4377024f22a7cd0451421dcd060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863042"
---
# <a name="disablepatchuninstall"></a><span data-ttu-id="40255-103">DisablePatchUninstall</span><span class="sxs-lookup"><span data-stu-id="40255-103">DisablePatchUninstall</span></span>

<span data-ttu-id="40255-104">Si cette [stratégie système](system-policy.md) par ordinateur est définie sur 1, les correctifs ne peuvent pas être supprimés de l’ordinateur par un utilisateur ou un administrateur.</span><span class="sxs-lookup"><span data-stu-id="40255-104">If this per-machine [system policy](system-policy.md) is set to 1, patches cannot be removed from the computer by a user or an administrator.</span></span> <span data-ttu-id="40255-105">La Windows Installer peut toujours supprimer un correctif qui n’est plus applicable à un produit.</span><span class="sxs-lookup"><span data-stu-id="40255-105">The Windows Installer can still remove a patch that is no longer applicable to a product.</span></span> <span data-ttu-id="40255-106">Si cette stratégie n’est pas définie, un utilisateur peut supprimer un correctif de l’ordinateur uniquement si l’utilisateur dispose des privilèges nécessaires pour supprimer le correctif.</span><span class="sxs-lookup"><span data-stu-id="40255-106">If this policy is not set, a user can remove a patch from the computer only if the user has been granted privileges to remove the patch.</span></span> <span data-ttu-id="40255-107">Cela peut dépendre du fait que l’utilisateur est un administrateur, si les paramètres de stratégie [DisableMsi](disablemsi.md) et [AlwaysInstallElevated a](alwaysinstallelevated.md) sont définis et si le correctif a été installé dans un contexte par utilisateur géré, non géré par utilisateur ou par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="40255-107">This can depend on whether the user is an administrator, whether [DisableMsi](disablemsi.md) and [AlwaysInstallElevated](alwaysinstallelevated.md) policy settings are set, and whether the patch was installed in a per-user managed, per-user unmanaged, or per-machine context.</span></span>

## <a name="registry-key"></a><span data-ttu-id="40255-108">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="40255-108">Registry Key</span></span>

<span data-ttu-id="40255-109">**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**</span><span class="sxs-lookup"><span data-stu-id="40255-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="40255-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="40255-110">Data Type</span></span>

<span data-ttu-id="40255-111">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="40255-111">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="40255-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="40255-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40255-113">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="40255-113">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



