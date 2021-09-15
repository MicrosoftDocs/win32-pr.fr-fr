---
description: La validation est effectuée lors de la compilation de l’effet. Pour valider la technique actuelle, spécifiez NULL comme handle de technique à valider.
ms.assetid: d1268f68-2893-4d7f-acd2-484346a20193
title: Validation (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecc64a17aba21af4b43bd41cc060a8711e5bb4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530973"
---
# <a name="validation-direct3d-9"></a>Validation (Direct3D 9)

La validation est effectuée lors de la compilation de l’effet. Pour valider la technique actuelle, spécifiez **null** comme handle de technique à valider.

La validation échoue pour l’un des éléments suivants :

-   Si le handle de technique spécifié n’existe pas.
-   Si l’application d’un État quelconque dans le cas d’un passage de la technique échoue.
-   Si la validation de l’appareil échoue après l’application de tous les États dans le cas d’un passage de la technique.
-   Si des nuanceurs non valides sont affectés aux États d’effet PIXELSHADER ou VERTEXSHADER dans n’importe quel passage de la technique.
-   Si les extrémités de l’appareil ne prennent pas en charge le mappage de cube et qu’une valeur de type textureCUBE est assignée à un état d’effet de TEXTURE, dans n’importe quelle étape de la technique.
-   Si les extrémités de l’appareil ne prennent pas en charge le mappage de volume et qu’une valeur de type texture3D est assignée à un état d’effet de TEXTURE, dans n’importe quelle étape de la technique.

Pour plus d’informations, consultez [États d’effet (Direct3D 9)](effect-states.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Format d’effet](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



