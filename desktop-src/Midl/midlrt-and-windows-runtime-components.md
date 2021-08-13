---
title: composants MIDLRT et Windows Runtime
description: montre comment créer des fichiers de métadonnées (. winmd) qui représentent l’API pour les composants de Windows Runtime personnalisés.
ms.assetid: 7830A5DB-9696-4A93-948B-51DA46A5143C
keywords:
- MIDL du compilateur MIDL
- midl du compilateur midl, midl et Windows Runtime winrt
- Windows Runtime MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f827178216bbb7e78c16f2c11fa68b29b2eb50cfc0714a0ed53b02ce5bdc4ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642903"
---
# <a name="midlrt-and-windows-runtime-components"></a>composants MIDLRT et Windows Runtime

montre comment créer des fichiers de métadonnées (. winmd) qui représentent l’API pour les composants de Windows Runtime personnalisés.


utilisez le compilateur MIDLRT pour générer des fichiers de métadonnées (. winmd) pour vos composants de Windows Runtime personnalisés.

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

 

 




