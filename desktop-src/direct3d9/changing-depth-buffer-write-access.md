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
# <a name="changing-depth-buffer-write-access-direct3d-9"></a>Modification de l’accès en écriture au tampon de profondeur (Direct3D 9)

Par défaut, le système Direct3D est autorisé à écrire dans le tampon de profondeur. La plupart des applications laissent l’écriture dans la mémoire tampon de profondeur activée, mais vous pouvez obtenir des effets spéciaux en n’autorisant pas le système Direct3D à écrire dans le tampon de profondeur.

Vous pouvez désactiver les écritures de mémoire tampon de profondeur en C++ en appelant la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) avec le paramètre d’état défini sur D3DRS \_ ZWRITEENABLE et le paramètre de valeur défini sur 0.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mémoires tampons de profondeur](depth-buffers.md)
</dt> </dl>

 

 
