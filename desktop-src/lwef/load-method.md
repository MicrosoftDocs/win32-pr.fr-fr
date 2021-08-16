---
title: Load, méthode
description: Load, méthode
ms.assetid: 72a37471-f69b-49a5-a6eb-d65bff970c0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e201053bf3eb9fbd7a3c5c7eb94f9b032cde13087f76e1fcfa176d068655137a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118748651"
---
# <a name="load-method"></a>Load, méthode

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Charge un caractère dans la collection de [**caractères**](/windows/desktop/lwef/the-characters-object) .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères. Load «**_CharacterID_*_»,_ *  *fournisseur*



| Partie          | Description                                                                                                                                                                                                                              |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Obligatoire. Valeur de chaîne que vous allez utiliser pour faire référence aux données caractères à charger.                                                                                                                                                  |
| *Fournisseur*    | Obligatoire. Type de données Variant qui doit être l’un des éléments suivants : **spécification** de l’emplacement du fichier local du fichier de définition du caractère spécifié. <br/> **URL** Adresse HTTP du fichier de définition du caractère.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Vous pouvez charger des caractères à partir du sous-répertoire de l’agent en spécifiant un chemin d’accès relatif (qui n’inclut pas de signe deux-points ou de barre oblique de début). cela a pour préfixe le chemin d’accès avec le répertoire de caractères de l’Agent (situé dans le répertoire local Windows \\ msagent). Par exemple, si vous spécifiez ce qui suit, génie. ACS est chargé à partir du répertoire de caractères de l’agent :


```
   Agent.Character.Load "genie", "genie.acs"
```



Vous pouvez également spécifier votre propre répertoire dans le répertoire de caractères de l’agent.


```
   Agent.Character.Load "genie", "MyCharacters\genie.acs"
```



Vous pouvez charger le caractère actuellement défini en tant que caractère par défaut de l’utilisateur actuel en n’incluant pas de chemin d’accès comme deuxième paramètre de la méthode **Load** .


```
   Agent.Character.Load "character"
```



Vous ne pouvez pas charger le même caractère (un caractère ayant le même GUID) plusieurs fois à partir d’une seule instance du contrôle. De même, vous ne pouvez pas charger le caractère par défaut et d’autres caractères en même temps à partir d’une seule instance du contrôle, car le caractère par défaut peut être identique à l’autre caractère. Si vous tentez de le faire, le serveur génère une erreur. Toutefois, vous pouvez créer une autre instance du contrôle de l’agent et charger le même caractère.

Microsoft Agent Fournisseur de données prend en charge le chargement de données de type caractère stockées dans un fichier structuré unique (. ACS) avec des données de caractères et des données d’animation, ainsi que des données de caractères distinctes (. ACF) et d’animation (. ). Utilisez l’unique structure structurée. Fichier ACS pour charger un caractère stocké sur un disque local ou un réseau et accessible à l’aide d’un protocole de fichiers conventionnel (tel que les chemins d’accès UNC). Utilisez le distinct. ACF et. Les fichiers de CCN lorsque vous souhaitez charger les fichiers d’animation individuellement à partir d’un site distant où ils sont accessibles à l’aide du protocole HTTP.

Pour. Les fichiers ACS, à l’aide de la méthode **Load** , permettent d’accéder aux animations d’un caractère. Pour. Fichiers ACF, vous utilisez également la méthode d' [**extraction**](get-method.md) pour charger des données d’animation. La méthode **Load** ne prend pas en charge le téléchargement. Fichiers ACS à partir d’un site HTTP.

Le chargement d’un caractère n’affiche pas automatiquement le caractère. Utilisez d’abord la méthode [**Show**](show-method.md) pour rendre le caractère visible.

Si vous utilisez la méthode **Load** pour charger un fichier de caractères stocké sur l’ordinateur local et que l’appel échoue ; par exemple, étant donné que le fichier est introuvable, l’agent génère une erreur. Vous pouvez utiliser la prise en charge dans votre langage de programmation pour fournir une routine de gestion des erreurs pour intercepter et traiter l’erreur.


```
   Sub Form_Load
      On Error GoTo ErrorHandler
      Agent1.Characters.Load "mychar", "genie.acs"
      ' Successful load
      . . .
      Exit Sub
      ErrorHandler:
      ' Unsuccessful load
      . . .
      Resume Next
   End Sub
```



Vous pouvez également gérer l’erreur en affectant à [**RaiseRequestErrors**](https://www.bing.com/search?q=**RaiseRequestErrors**) la **valeur false**, en déclarant un objet et en lui assignant la demande de **chargement** . Suivez ensuite l’appel de **chargement** avec une instruction qui vérifie l’état de l’objet de [**requête**](/windows/desktop/lwef/the-request-object) .


```
Dim LoadRequest as Object

   Sub Form_Load
      Agent1.RaiseRequestErrors = False
      Set LoadRequest = Agent1.Characters.Load _
         ("mychar", "c:\some directory\some character.acs")
      If LoadRequest.Status Not 0 Then
         ' Unsuccessful load
         . . .
         Exit Sub
      Else 
         ' Successful load
         . . .
   End Sub
```



Si vous chargez un caractère qui n’est pas local ; par exemple, à l’aide du protocole HTTP, vous pouvez également rechercher un échec de **chargement** en affectant un objet de [**requête**](/windows/desktop/lwef/the-request-object) à la méthode **Load** . Toutefois, étant donné que cette méthode de chargement d’un caractère est gérée de façon asynchrone, vérifiez son état dans l’événement [**RequestComplete**](requestcomplete-event.md) . Cette technique ne fonctionne pas en chargeant un caractère à l’aide du protocole UNC, car la méthode **Load** est traitée de façon synchrone.

 

