---
description: Si cette stratégie système par utilisateur est définie sur &\# 0034 ; 1&\# 0034 ;; le programme d’installation recherche les fichiers de transformation à la racine de toutes les sources réseau dans la liste source du produit. Par défaut, les transformations sont stockées dans le dossier Application Data du profil d’un utilisateur.
ms.assetid: 24881078-1610-4a37-a52d-fcabd78e1738
title: Stratégie TransformsAtSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91be9c56f2e68a27d904acf98088204dc4012b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111991"
---
# <a name="transformsatsource-policy"></a><span data-ttu-id="93371-104">Stratégie TransformsAtSource</span><span class="sxs-lookup"><span data-stu-id="93371-104">TransformsAtSource Policy</span></span>

<span data-ttu-id="93371-105">Si cette [stratégie système](system-policy.md) par utilisateur est définie sur « 1 »; le programme d’installation recherche les fichiers de transformation à la racine de toutes les sources réseau dans la liste source du produit.</span><span class="sxs-lookup"><span data-stu-id="93371-105">If this per-user [system policy](system-policy.md) is set to "1"; the installer searches for transform files in the root of any network sources in the source list for the product.</span></span> <span data-ttu-id="93371-106">Par défaut, les transformations sont stockées dans le dossier Application Data du profil d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="93371-106">By default, transforms are stored in the Application Data folder of a user's profile.</span></span>

<span data-ttu-id="93371-107">Windows Installer interprète la stratégie TransformsAtSource comme étant identique à la [stratégie TransformsSecure](transformssecure-policy.md).</span><span class="sxs-lookup"><span data-stu-id="93371-107">Windows Installer interprets the TransformsAtSource policy to be the same as the [TransformsSecure policy](transformssecure-policy.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="93371-108">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="93371-108">Registry Key</span></span>

<span data-ttu-id="93371-109">**HKEY \_ \_** \\ **Stratégies logicielles** de l’utilisateur actuel \\  \\ **Microsoft** \\ **Windows** \\ **installer**</span><span class="sxs-lookup"><span data-stu-id="93371-109">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="93371-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="93371-110">Data Type</span></span>

<span data-ttu-id="93371-111">**SZ de REG \_**</span><span class="sxs-lookup"><span data-stu-id="93371-111">**REG\_SZ**</span></span>

 

 



