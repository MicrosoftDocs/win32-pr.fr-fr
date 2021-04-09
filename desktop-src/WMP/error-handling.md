---
title: Gestion des erreurs (Windows Media Player SDK)
description: Gestion des erreurs
ms.assetid: f0567c77-a855-4b93-9fb7-a36cde63859f
keywords:
- Lecteur Windows Media, gestion des erreurs
- Windows Media Player Object Model, gestion des erreurs
- modèle objet, gestion des erreurs
- Contrôle ActiveX du lecteur Windows Media, gestion des erreurs
- Contrôle ActiveX, gestion des erreurs
- Contrôle ActiveX Windows Media Player Mobile, gestion des erreurs
- Windows Media Player Mobile, gestion des erreurs
- Guide de migration, gestion des erreurs
- gestion des erreurs dans le modèle objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f3b96e04d24009ee4b7e5819fdb26dfd6effd63
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102625"
---
# <a name="error-handling-windows-media-player-sdk"></a>Gestion des erreurs (Windows Media Player SDK)

Le contrôle ActiveX du lecteur Windows Media 6,4 fournit la gestion des erreurs par défaut en affichant les messages d’erreur dans les boîtes de dialogue et dans la barre d’État. Vous pouvez également fournir une gestion personnalisée des erreurs en traitant les erreurs dans votre script. La gestion des erreurs est pilotée par les événements, ce qui signifie que vous recevez une notification pour chaque erreur et que vous devez décider comment traiter chaque événement d’erreur lorsqu’il se produit. Pour plus d’informations sur la gestion des erreurs à l’aide du modèle d’objet de la version 6,4, consultez la section gestion des erreurs du Guide du modèle d’objet du lecteur version 6,4, qui fait partie du kit de développement logiciel (SDK) du lecteur Windows Media.

Le modèle objet Windows Media Player 7 ou version ultérieure fournit l’objet d' **erreur** et l’objet **ErrorItem** pour gérer les erreurs. Ces deux objets fonctionnent ensemble pour vous fournir un mécanisme de gestion des erreurs qui vous donne un contrôle complet et flexible du processus de gestion des erreurs. L’objet **Error** donne accès à une collection d’objets **ErrorItem** ; chaque objet **ErrorItem** fournit des détails sur un message d’erreur individuel.

Lorsqu’une erreur se produit, les informations sur l’erreur sont publiées dans une file d’attente d’erreurs. La file d’attente est une collection d’objets **ErrorItem** . À mesure que chaque erreur est ajoutée à la file d’attente, elle est associée à un numéro d’index (commençant par zéro) qui peut être utilisé pour identifier l’objet **ErrorItem** particulier. *Erreur*. la propriété **errorCount** récupère le nombre d’erreurs dans la file d’attente d’erreurs. Étant donné que les numéros d’index sont de base zéro, l’erreur la plus récente publiée dans la file d’attente aura toujours une valeur d’index égale à *Error*. **errorCount** moins un.

Vous pouvez créer un gestionnaire d’événements d’erreur pour le lecteur Windows Media à l’aide d’un script. L’exemple JScript suivant montre comment récupérer l’élément d’erreur le plus récent de la file d’attente d’erreurs et afficher le code d’erreur et la description d’erreur à l’aide du modèle objet Windows Media Player 7 ou version ultérieure. L’objet **lecteur** a été créé avec l’ID = « wmp9 ».


```C++
<!-- Create an error event handler for Windows Media Player 7 or later errors. -->
<SCRIPT  LANGUAGE = "JScript"  FOR = WMP9  EVENT = error()>

// Store the number of errors in the error queue.
var max = WMP9.error.errorCount;

// Retrieve most recent ErrorItem object.
var err = WMP9.error.item(max-1)

// Store the error code number.
var errNum = err.errorCode;

// Store the error description string.
var errDesc = err.errorDescription;

// Build a message string to notify the user.
var msg = "Error number: " + errNum + "\n";
msg += "Error description: " + errDesc;

// Display the message box.
alert(msg);

</SCRIPT>

```



L’objet **Error** a deux méthodes supplémentaires que vous pouvez utiliser. *Erreur*. la méthode **clearErrorQueue** vous permet de supprimer toutes les erreurs de la file d’attente d’erreurs et de réinitialiser le numéro d’index à zéro. Vous avez un contrôle total sur ce processus ; vous pouvez conserver les erreurs dans la file d’attente tant que vous en avez besoin pour qu’elles soient disponibles, puis vider la file d’attente lorsque vous avez terminé de traiter les erreurs.

*Erreur*. la méthode **Webhelp** offre un moyen d’afficher les informations les plus récentes sur l’erreur à l’utilisateur à l’aide d’Internet. Lorsqu’elle est appelée, cette méthode transfère toutes les informations pertinentes sur la première erreur de la file d’attente (celle avec l’index zéro) à l’aide Web du lecteur Microsoft Windows Media, qui affiche des informations supplémentaires sur l’erreur dans la fenêtre du navigateur active.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Error, objet**](error-object.md)
</dt> <dt>

[**Objet ErrorItem**](erroritem-object.md)
</dt> <dt>

[**Guide de migration du modèle objet**](object-model-migration-guide.md)
</dt> </dl>

 

 




