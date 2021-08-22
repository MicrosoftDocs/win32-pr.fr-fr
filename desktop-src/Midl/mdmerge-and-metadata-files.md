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
ms.openlocfilehash: 1a065a8ff93485728b1c5c4c0c7b43de88e3844a8a013f07caee8d85d76d721d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119252429"
---
# <a name="mdmerge-and-metadata-files"></a>Fichiers de métadonnées et MDMERGE

Compose plusieurs fichiers de métadonnées (. winmd) en un certain nombre de fichiers de métadonnées de sortie, en fonction de l’espace de noms.

## <a name="usage"></a>Usage

Exécutez MDMERGE à partir de la ligne de commande à l’aide de la commande suivante :

**mdmerge**  *<* **options**_>_

où * < ***options** _>_ représente les options de ligne de commande que vous souhaitez utiliser.

générez des fichiers de métadonnées pour vos composants de Windows Runtime personnalisés à l’aide du compilateur MIDLRT. pour plus d’informations, consultez [MIDLRT et Windows Runtime components](midlrt-and-windows-runtime-components.md).

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

## <a name="remarks"></a>Remarques

la composition des métadonnées permet à plusieurs fichiers IDL de contenir des définitions pour Windows Runtime composants dans le même espace de noms. Cela vous évite de définir tous les types dans un espace de noms au sein d’un seul fichier IDL.

vous pouvez avoir de nombreux composants de Windows Runtime que vos applications utilisent. lorsque vous effectuez l’étape finale pour produire des assemblys de métadonnées Windows Runtime déployables, vous pouvez configurer MDMERGE pour fusionner des composants à partir de plusieurs répertoires de métadonnées, comme ceux qui sont installés avec le système (% Windows% \\ system32 \\ WinMetadata), vos types de fondation et le répertoire de build de votre projet actuel. tous les types nécessaires sont fusionnés dans les assemblys de métadonnées appropriés et déployables que vous pouvez empaqueter pour le magasin de Windows.

Vous pouvez utiliser l’option [**/n**](-mdmerge-n.md) pour spécifier la profondeur d’espace de noms prise en charge pour composer des assemblys de métadonnées. cela permet de configurer une division à chaud pour vos composants Windows Runtime, afin qu’un seul fichier. winmd soit empaqueté au lieu de plusieurs. cela réduit les temps de chargement et d’e/s de fichier requis par vos applications Windows store.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[composants MIDLRT et Windows Runtime](midlrt-and-windows-runtime-components.md)
</dt> </dl>

 

 




