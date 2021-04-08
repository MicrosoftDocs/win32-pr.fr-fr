---
description: Le moyen le plus simple de créer un espace de noms consiste à utiliser du code format MOF (MOF) pour créer l’espace de noms dans le répertoire actif. Le répertoire actif est défini lorsque vous vous connectez.
ms.assetid: 2b83cd96-079f-4178-9e5a-68ede3a92066
ms.tgt_platform: multiple
title: Création d’un espace de noms enfant avec du code MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f80aa04e2ef4f5c7bbfc43d9020727b3b2a6e0d
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104042972"
---
# <a name="creating-a-child-namespace-with-mof-code"></a>Création d’un espace de noms enfant avec du code MOF

Le moyen le plus simple de créer un espace de noms consiste à utiliser du code format MOF (MOF) pour créer l’espace de noms dans le répertoire actif. Le répertoire actif est défini lorsque vous vous connectez.

La procédure suivante décrit comment créer un espace de noms enfant à l’aide de code MOF.

**Pour créer un espace de noms enfant à l’aide du code MOF**

1.  Créez une instance de la classe d' [**\_ \_ espace de noms**](--namespace.md) .

    L’exemple de code suivant montre comment créer un espace de noms enfant.

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
    };
    ```

2.  Si vous souhaitez exiger de l’utilisateur qu’il établisse une connexion chiffrée à l’espace de noms, utilisez le qualificateur **RequiresEncryption** . Pour plus d’informations, consultez [la page exiger une connexion chiffrée à un espace de noms](requiring-an-encrypted-connection-to-a-namespace.md).

    L’exemple de code suivant montre comment exiger une connexion chiffrée.

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
        [RequiresEncryption(TRUE)] 
        instance of __MyNamespace { };
    };
    ```

3.  Si vous souhaitez définir un descripteur de sécurité sur l’espace de noms plutôt que d’utiliser la sécurité par défaut de l’espace de noms, utilisez le qualificateur **NamespaceSecuritySDDL** . Pour plus d’informations, consultez [définition de la sécurité de l’espace de noms lors de la création de l’espace de noms](setting-namespace-security-when-the-namespace-is-created.md).

    L’exemple de code suivant montre comment définir un descripteur de sécurité sur l’espace de noms.

    ``` syntax
    #pragma namespace("\\\\.\\root\\MyNamespace")

    [NamespaceSecuritySDDL ("O:AUG:AUD:(A;CI;0x00060033;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

4.  Compilez et chargez l’instance d' [**\_ \_ espace de noms**](--namespace.md) à l’aide de l’utilitaire [mofcomp](mofcomp.md) ou de l’interface [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) . Mofcomp et l’interface **IMofCompiler** chargent automatiquement l’espace de noms dans le répertoire actif. Pour plus d’informations, consultez [compilation des fichiers MOF](compiling-mof-files.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Qualificateurs WMI standard**](standard-wmi-qualifiers.md)
</dt> </dl>

 

 



