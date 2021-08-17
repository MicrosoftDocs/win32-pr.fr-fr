---
description: Options de format de fichier X, de chargement et d’enregistrement.
ms.assetid: 813a2b4b-6577-4cdf-a2e6-e06870638354
title: D3DXF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d286ad4cf64133683de026893beb9fa081899e6b170e4b3adb478798eb4b3edf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118096074"
---
# <a name="d3dxf"></a>D3DXF

Options de format de fichier X, de chargement et d’enregistrement.

## <a name="file-formats"></a>Formats de fichier

Le tableau suivant spécifie le type de données de fichier :



| \#définit le format de fichier     | Valeur | Description                                                                                    |
|-------------------------------|-------|------------------------------------------------------------------------------------------------|
| D3DXF \_ FILEFORMAT \_ binaire     | 0     | Fichier binaire au format hérité. Consultez [référence de fichier X (héritée)](dx9-graphics-reference-x-file.md). |
| \_Texte du FILEFORMAT D3DXF \_       | 1     | Fichier texte.                                                                                     |
| D3DXF \_ FILEFORMAT \_ compressé | 2     | Fichier compressé. Avec cet indicateur, vous devez également spécifier le format binaire ou le format texte.   |



 

## <a name="file-load-options"></a>Options de chargement de fichier

Le tableau suivant spécifie les options de chargement de fichier avec des fichiers. x :



| \#définition                      | Valeur | Description                |
|-------------------------------|-------|----------------------------|
| D3DXF \_ FILELOAD \_ FromFile     | 0     | Charger des données à partir d’un fichier.     |
| D3DXF \_ FILELOAD \_ FROMWFILE    | 1     | Charger des données à partir d’un fichier.     |
| D3DXF \_ FILELOAD \_ FROMRESOURCE | 2     | Charger des données à partir d’une ressource. |
| D3DXF \_ FILELOAD \_ FROMMEMORY   | 3     | Chargez des données à partir de la mémoire.     |



 

## <a name="file-save-options"></a>Options d’enregistrement de fichier

Le tableau suivant spécifie les options d’enregistrement et de chargement de fichiers avec des fichiers. x :



| \#définition                 | Valeur | Description                    |
|--------------------------|-------|--------------------------------|
| D3DXF \_ FichierEnregistrer \_ TOFILE  | 0     | Enregistrer dans un fichier.                |
| D3DXF \_ FichierEnregistrer \_ TOWFILE | 1     | Enregistrez dans un fichier à caractères larges. |



 

## <a name="constant-information"></a>Informations constantes



| Condition requise                         | Valeur           |
|--------------------------|------------|
| En-tête                   | d3dx9xof. h |
| Système d’exploitation minimal | Windows 98 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes de fichier D3DX X](dx9-graphics-reference-d3dx-x-file-constants.md)
</dt> <dt>

[**D3DXSaveMeshToX**](d3dxsavemeshtox.md)
</dt> </dl>

 

 



