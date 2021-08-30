---
description: Une autre façon de créer un espace de noms consiste à utiliser du code format MOF (MOF) pour créer un espace de noms frère. Un espace de noms frère est un espace de noms qui n’existe pas en tant qu’enfant de l’espace de noms actuel.
ms.assetid: 1a3f8569-e725-4158-9a2b-b440b9247925
ms.tgt_platform: multiple
title: Création d’un espace de noms frère avec du code MOF
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 282ac9f23abcfb98c9c46d6030d679235d838208e4934366c2e10a0380a5df0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071489"
---
# <a name="creating-a-sibling-namespace-with-mof-code"></a>Création d’un espace de noms frère avec du code MOF

Une autre façon de créer un espace de noms consiste à utiliser du code format MOF (MOF) pour créer un espace de noms frère. Un espace de noms frère est un espace de noms qui n’existe pas en tant qu’enfant de l’espace de noms actuel.

La procédure suivante décrit comment créer un espace de noms frère avec du code MOF.

**Pour créer un espace de noms frère avec du code MOF**

1.  Insérez la commande [**\# pragma namespace**](pragma-namespace.md) dans votre code MOF avant la déclaration d’espace de noms.

    La commande [**\# pragma namespace**](pragma-namespace.md) indique à WMI où créer les instances à la suite de la directive.

2.  Créez une instance de la classe d' [**\_ \_ espace de noms**](--namespace.md) .
3.  Compilez votre code à l’aide de l’utilitaire [mofcomp](mofcomp.md) ou de l’interface [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .

    Pour plus d’informations, consultez [compilation des fichiers MOF](compiling-mof-files.md).

L’exemple de code MOF suivant décrit comment créer un espace de noms en tant que frère de l’espace de noms « root \\ cimv2 ».

``` syntax
#pragma namespace("\\\\.\\Root")

instance of __Namespace 
{
    Name = "MyNamespace";
};
```

 

 



