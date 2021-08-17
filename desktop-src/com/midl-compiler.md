---
title: Compilateur MIDL
description: Compilateur MIDL
ms.assetid: ce3d40b7-49fd-4689-9100-fdbad4f0c557
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db4afbbe8c7a82f4335855b40e578fe2eea046fa4c7f0560e3e297b559a67ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736428"
---
# <a name="midl-compiler"></a>Compilateur MIDL

Le compilateur MIDL traite un fichier IDL pour générer une bibliothèque de types et des fichiers de sortie. Le type des fichiers de sortie générés par le compilateur MIDL dépend des attributs spécifiés dans la liste d’attributs d’interface du fichier IDL.

Si la liste d’attributs contient le \[ [](/windows/desktop/Midl/object) \] mot clé Object, le compilateur MIDL génère des fichiers de sortie de l’interface com : un fichier de proxy d’interface, un fichier d’en-tête d’interface et un fichier d’identificateur global unique (Guid) pour l’interface. Si le fichier IDL contient une instruction de [**bibliothèque**](/windows/desktop/Midl/library) , MIDL génère un fichier de bibliothèque de types avec l’extension de nom de fichier. tlb. Si le fichier IDL contient des interfaces qui n’ont pas le \[  \] mot clé Object et qui ne sont pas incluses dans une instruction **Library** , le compilateur MIDL génère des fichiers de sortie d’interface appropriés pour les appels de procédure distante (RPC) : un fichier stub client, un fichier stub de serveur et un fichier d’en-tête. Pour plus d’informations, consultez les rubriques [définitions d’interface et bibliothèques de types](/windows/desktop/Midl/interface-definitions-and-type-libraries) et génération d' [une bibliothèque de types avec MIDL](/windows/desktop/Midl/generating-a-type-library-with-midl-2).

Pour générer une bibliothèque de types et des fichiers de sortie à partir d’un fichier IDL :

-   À partir de l’invite de commandes, exécutez

     *nom de fichier* MIDL

    où *filename* est le nom du fichier IDL.

Le compilateur MIDL prend également en charge plusieurs paramètres facultatifs. Pour obtenir une liste complète, consultez « Référence de Command-Line MIDL » dans la documentation de Visual C++, ou exécutez la ligne de commande suivante :

**MIDL/ ?**

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Microsoft Interface Definition Language](/windows/desktop/Midl/midl-start-page)
</dt> <dt>

[Traduire en C++](translating-to-c--.md)
</dt> </dl>

 

 