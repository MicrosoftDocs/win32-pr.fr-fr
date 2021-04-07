---
title: Fichiers de métadonnées et MDMERGE
description: Compose plusieurs fichiers de métadonnées (. winmd) en un certain nombre de fichiers de métadonnées de sortie, en fonction de l’espace de noms.
ms.assetid: A3203627-82DF-4744-BBBC-53D13F30210E
keywords:
- metadata
- fichier winmd
- Métadonnées Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2d91f8c7506dd80fd2477beb61c5b99a26b05b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939697"
---
# <a name="mdmerge-and-metadata-files"></a>Fichiers de métadonnées et MDMERGE

Compose plusieurs fichiers de métadonnées (. winmd) en un certain nombre de fichiers de métadonnées de sortie, en fonction de l’espace de noms.

## <a name="usage"></a>Utilisation

Exécutez MDMERGE à partir de la ligne de commande à l’aide de la commande suivante :

 *< ***options*** de mdmerge>*

où *<  options >* représente les options de ligne de commande que vous souhaitez utiliser.

Générez des fichiers de métadonnées pour vos composants de Windows Runtime personnalisés à l’aide du compilateur MIDLRT. Pour plus d’informations, consultez [MIDLRT et Windows Runtime Components](midlrt-and-windows-runtime-components.md).

## <a name="command-line-switches"></a>Commutateurs de ligne de commande

La liste suivante répertorie les commutateurs de ligne de commande utilisés par MDMERGE.

<dl>

[**/i**](-mdmerge-i.md)  
[**/Metadata \_ dir**](-mdmerge-metadata-dir.md)  
[**/n**](-mdmerge-n.md)  
[**/o**](-mdmerge-o.md)  
[**/partial**](-mdmerge-partial.md)  
[**/f**](-mdmerge-v.md)  
</dl>

Une liste complète des commutateurs et options du compilateur MDMERGE est disponible lorsque vous utilisez les options **-h** et **/ ?** Active.

## <a name="remarks"></a>Notes

La composition des métadonnées permet à plusieurs fichiers IDL de contenir des définitions pour Windows Runtime composants dans le même espace de noms. Cela vous évite de définir tous les types dans un espace de noms au sein d’un seul fichier IDL.

Vous pouvez avoir de nombreux composants de Windows Runtime que vos applications utilisent. Lorsque vous effectuez l’étape finale pour produire des assemblys de métadonnées Windows Runtime déployables, vous pouvez configurer MDMERGE pour fusionner des composants à partir de plusieurs répertoires de métadonnées, comme ceux qui sont installés avec le système (% WINDOWS% \\ system32 \\ WinMetadata), vos types de fondation et le répertoire de build de votre projet actuel. Tous les types nécessaires sont fusionnés dans les assemblys de métadonnées appropriés et déployables que vous pouvez empaqueter pour le Windows Store.

Vous pouvez utiliser l’option [**/n**](-mdmerge-n.md) pour spécifier la profondeur d’espace de noms prise en charge pour composer des assemblys de métadonnées. Cela permet de configurer une division à chaud pour vos composants Windows Runtime, afin qu’un seul fichier. winmd soit empaqueté au lieu de plusieurs. Cela réduit le temps de chargement et l’e/s de fichier requis par vos applications du Windows Store.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Composants MIDLRT et Windows Runtime](midlrt-and-windows-runtime-components.md)
</dt> </dl>

 

 




