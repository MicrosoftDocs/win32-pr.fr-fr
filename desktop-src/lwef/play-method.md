---
title: Méthode Play (fonctionnalités héritées de l’environnement Windows)
description: Méthode Play
ms.assetid: 7e89341a-b4d3-4bea-8e7f-31c649ff06b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d06f4275d7b4c0959a59536c8b20a95c14ab1c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106511529"
---
# <a name="play-method-legacy-windows-environment-features"></a>Méthode Play (fonctionnalités héritées de l’environnement Windows)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Lit l’animation spécifiée pour le caractère spécifié.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («**_CharacterID_*_»). Play_* «*AnimationName*»

</dd> </dl> 

| Partie            | Description                                                          |
|-----------------|----------------------------------------------------------------------|
| *AnimationName* | Obligatoire. Chaîne qui spécifie le nom d’une séquence d’animation. |



 

## <a name="remarks"></a>Notes

Le nom d’une animation est défini lorsque le caractère est compilé à l’aide de l’éditeur de caractères Microsoft Agent. Avant de lire l’animation spécifiée, le serveur tente de lire l’animation de **retour** pour l’animation précédente, si celle-ci a été assignée.

Lors de l’accès aux animations d’un caractère à l’aide d’un protocole de fichier conventionnel, vous pouvez simplement utiliser la méthode **Play** en spécifiant le nom de l’animation. Toutefois, si vous utilisez le protocole HTTP pour accéder aux données d’animation de caractères, utilisez la méthode d' **extraction** pour charger l’animation avant d’appeler la méthode **Play** .

Pour plus d’informations, consultez la méthode **obtenir** .

Pour simplifier votre syntaxe, vous pouvez déclarer une référence d’objet et la définir pour faire référence à l’objet de [**caractère**](/windows/desktop/lwef/the-characters-object) dans la collection de [**caractères**](/windows/desktop/lwef/the-characters-object) et utiliser la référence dans le cadre de vos instructions de **lecture** :


```
   Dim Genie   
   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")
   
   Genie.Get "state", "Showing"
   Genie.Show

   Genie.Get "animation", "Greet, GreetReturn"
   Genie.Play "Greet"
   Genie.Speak "Hello."
```



Si vous déclarez une référence d’objet et que vous la définissez sur cette méthode, elle retourne un objet de [**requête**](/windows/desktop/lwef/the-request-object) . En outre, si vous spécifiez une animation qui n’est pas chargée ou si le caractère n’a pas été chargé avec succès, le serveur définit la propriété [**Status**](status-property.md) de l’objet **Request** sur « failed » avec un numéro d’erreur approprié. Toutefois, si l’animation n’existe pas et que les données du caractère ont déjà été chargées avec succès, le serveur génère une erreur.

La méthode **Play** ne rend pas visible le caractère. Si le caractère n’est pas visible, le serveur lit l’animation de manière invisible et définit la propriété [**Status**](status-property.md) de l’objet de [**requête**](/windows/desktop/lwef/the-request-object) .

 

 
