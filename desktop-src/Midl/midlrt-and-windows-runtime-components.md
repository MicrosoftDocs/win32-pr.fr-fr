---
title: Composants MIDLRT et Windows Runtime
description: Montre comment créer des fichiers de métadonnées (. winmd) qui représentent l’API pour les composants de Windows Runtime personnalisés.
ms.assetid: 7830A5DB-9696-4A93-948B-51DA46A5143C
keywords:
- MIDL du compilateur MIDL
- MIDL du compilateur MIDL, MIDL et Windows Runtime WinRT
- Windows Runtime MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edf4d40b3fc5b0a5ed8eeb9b5fd47a3b87c4543
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104508201"
---
# <a name="midlrt-and-windows-runtime-components"></a>Composants MIDLRT et Windows Runtime

Montre comment créer des fichiers de métadonnées (. winmd) qui représentent l’API pour les composants de Windows Runtime personnalisés.


Utilisez le compilateur MIDLRT pour générer des fichiers de métadonnées (. winmd) pour vos composants de Windows Runtime personnalisés.

Lorsque vos fichiers de métadonnées sont générés, vous pouvez les composer dans un package plus efficace à l’aide de l’utilitaire MDMERGE. Pour plus d’informations, consultez [MDMERGE et fichiers de métadonnées](mdmerge-and-metadata-files.md).


L’utilisation de MIDLRT est similaire à l’utilisation du compilateur MIDL. Exécutez MIDLRT à partir de la ligne de commande à l’aide de la commande suivante :

**midlrt**  *<* **options** _>_ **nom de fichier. idl**

où * < ***options** _>_ représente les options de ligne de commande que vous souhaitez utiliser, et nom_fichier. idl est le nom du fichier IDL à compiler.


La liste suivante répertorie les commutateurs de ligne de commande que MIDLRT.EXE utilise.

<dl>

[**/enum ( \_ classe)**](-enum-class.md)  
[**/Metadata \_ dir**](-metadata-dir.md)  
[**/nomidl**](-nomidl.md)  
[**/nomd**](-nomd.md)  
[**préfixe/NS \_**](-ns-prefix.md)  
[**/winmd**](-winmd.md)  
[**/WinRT**](-winrt.md)  
</dl>

Une liste complète des commutateurs et options du compilateur MIDLRT est disponible lorsque vous utilisez le compilateur MIDLRT [**/Help**](-help-.md) et/ ? Active. Les commutateurs sont organisés par catégories. Pour plus d’informations, consultez la [Référence du Command-Line MIDL](midl-command-line-reference.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fichiers de métadonnées et MDMERGE](mdmerge-and-metadata-files.md)
</dt> </dl>

 

 




