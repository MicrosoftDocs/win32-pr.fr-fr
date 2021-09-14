---
description: Vous pouvez maintenant créer automatiquement un mipmap qui est une série de textures, chacune filtrée avec une résolution différente.
ms.assetid: ae5955f9-e52a-41d7-a199-800e37a3e936
title: Génération automatique de des mipmaps (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fda5b765d42ffa10f8cc5998daa66ae36c2bc75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126998740"
---
# <a name="automatic-generation-of-mipmaps-direct3d-9"></a>Génération automatique de des mipmaps (Direct3D 9)

Vous pouvez maintenant créer automatiquement un mipmap qui est une série de textures, chacune filtrée avec une résolution différente. Les des mipmaps sont généralement utilisés pour fournir des niveaux de détail différents lors du rendu. La génération automatique de des mipmaps au moment de la création de la texture tire parti du filtrage matériel, car le mipmap réside dans la mémoire vidéo.

Pour générer automatiquement un mipmap, définissez un nouveau D3DUSAGE d’utilisation [ \_ AUTOGENMIPMAP](d3dusage.md) avant d’appeler [**CreateTexture**](/windows/desktop/api). La génération de sous-niveau à partir de ce point sur est complètement transparente pour l’application. Seul le niveau de texture supérieur est accessible à l’application ; les sous-niveaux de texture ne sont pas accessibles, car ils sont créés uniquement lorsque le pilote en a besoin. Dans les cas où la génération de sous-niveaux peut prendre beaucoup de temps, utilisez [**GenerateMipSubLevels**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-generatemipsublevels) pour indiquer au pilote qu’il doit générer des sous-niveaux à un moment approprié pour l’application.

## <a name="mipmap-filtering"></a>Filtrage mipmap

[**SetAutoGenFilterType**](/windows/desktop/api) contrôle la qualité du filtrage lors de la génération automatique. La modification du type de filtre met les sous-niveaux mipmap en valeur et provoque leur régénération. Utilisez [**GetAutoGenFilterType**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-getautogenfiltertype) pour récupérer le type de filtre actuel. Le type de filtre par défaut est D3DTEXF \_ Linear. Si le pilote ne prend pas en charge un filtre linéaire, le type de filtre est défini sur D3DTEXF \_ point.

Ces méthodes n’ont aucun effet si la texture n’est pas créée avec [D3DUSAGE \_ AUTOGENMIPMAP](d3dusage.md) et qu’aucun échec n’est retourné. Tous les types de filtre pris en charge par le pilote pour le filtrage de texture normal sont pris en charge pour la génération automatique, à l’exception de D3DTEXF \_ None. Pour chaque type de ressource, les pilotes doivent prendre en charge tous les types de filtres signalés dans les limites de filtre texture, CubeTexture et volumetexture correspondantes.

Pour vérifier les types de filtre pris en charge, consultez les limites prises en charge par les membres TextureFilterCaps et/ou CubeTextureFilterCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="mipmap-support"></a>Prise en charge du mipmap

[D3DUSAGE \_ AUTOGENMIPMAP](d3dusage.md) n’est qu’une indication, et la spécification de cette option lors de la création d’une texture ou lors de l’appel de [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) ne provoque pas d’erreur sur l’un des types d’interface de pilote de périphérique (DDI).

L’appel de [**UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) est illégal lorsque la source est un mipmap généré automatiquement, mais que la destination n’est pas. La source peut être un mipmap non généré automatiquement et la destination peut être un mipmap généré automatiquement. Dans ce cas, seul le niveau de correspondance le plus élevé est mis à jour. Tous les autres sous-niveaux source sont ignorés. De même, lorsque la source et la destination sont générées automatiquement, seul le niveau de correspondance le plus élevé est mis à jour. Les sous-niveaux de la source sont ignorés et les sous-niveaux de destination sont régénérés.

Pour vérifier la prise en charge de la génération automatique de des mipmaps, vérifiez que [D3DCAPS2 \_ CANAUTOGENMIPMAP](d3dcaps2.md) est défini. Si c’est le cas, appelez [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) avec [D3DUSAGE \_ AUTOGENMIPMAP](d3dusage.md). Si la valeur de retour est D3D \_ OK, il est garanti que les des mipmaps sont générés automatiquement. Si la valeur de retour est D3DOK \_ NOAUTOGEN, cela signifie que l’appel de Create va échouer, mais qu’aucun des mipmaps n’est généré.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Textures Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
