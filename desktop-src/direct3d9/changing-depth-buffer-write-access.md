---
description: Par défaut, le système Direct3D est autorisé à écrire dans le tampon de profondeur. La plupart des applications laissent l’écriture dans la mémoire tampon de profondeur activée, mais vous pouvez obtenir des effets spéciaux en n’autorisant pas le système Direct3D à écrire dans le tampon de profondeur.
ms.assetid: d426ebff-bfce-4e5b-a97b-7b2539b4a9de
title: Modification de l’accès en écriture au tampon de profondeur (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504a261c4d30c9d0bd9edfbf07f765b2037e8195
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516373"
---
# <a name="changing-depth-buffer-write-access-direct3d-9"></a><span data-ttu-id="3f6f6-104">Modification de l’accès en écriture au tampon de profondeur (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3f6f6-104">Changing Depth Buffer Write Access (Direct3D 9)</span></span>

<span data-ttu-id="3f6f6-105">Par défaut, le système Direct3D est autorisé à écrire dans le tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-105">By default, the Direct3D system is allowed to write to the depth buffer.</span></span> <span data-ttu-id="3f6f6-106">La plupart des applications laissent l’écriture dans la mémoire tampon de profondeur activée, mais vous pouvez obtenir des effets spéciaux en n’autorisant pas le système Direct3D à écrire dans le tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-106">Most applications leave writing to the depth buffer enabled, but you can achieve some special effects by not allowing the Direct3D system to write to the depth buffer.</span></span>

<span data-ttu-id="3f6f6-107">Vous pouvez désactiver les écritures de mémoire tampon de profondeur en C++ en appelant la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) avec le paramètre d’état défini sur D3DRS \_ ZWRITEENABLE et le paramètre de valeur défini sur 0.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-107">You can disable depth buffer writes in C++ by calling the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method with the State parameter set to D3DRS\_ZWRITEENABLE and the Value parameter set to 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f6f6-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3f6f6-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f6f6-109">Mémoires tampons de profondeur</span><span class="sxs-lookup"><span data-stu-id="3f6f6-109">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
