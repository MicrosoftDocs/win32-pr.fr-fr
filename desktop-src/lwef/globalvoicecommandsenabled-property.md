---
title: Propriété GlobalVoiceCommandsEnabled
description: Propriété GlobalVoiceCommandsEnabled
ms.assetid: d4f74019-fa33-41fc-abe7-01791ff188f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f889d242afca406ba443fd3d9a19afb837fbed0390f5c0c3d2bbd2ac2ccbccb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751443"
---
# <a name="globalvoicecommandsenabled-property"></a>Propriété GlobalVoiceCommandsEnabled

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit si la voix est activée pour les commandes globales de l’agent.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agents. ***caractères («**_CharacterID_*_»). Commands. GlobalVoiceCommandsEnabled_*

\[ = *expression*\]



| Partie      | Description                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Expression booléenne qui indique si les paramètres vocaux pour les commandes globales de l’agent sont activés. **True** (par défaut) les paramètres vocaux sont activés. <br/> **Valeur false** Les paramètres vocaux sont désactivés.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Microsoft Agent ajoute automatiquement des paramètres vocaux (grammaire) pour l’ouverture et la fermeture de la fenêtre commandes vocales et pour l’affichage et le masquage du caractère. Si vous affectez à **GlobalVoiceCommandsEnabled** la **valeur false**, agent désactive tous les paramètres vocaux pour ces commandes, ainsi que les paramètres vocaux pour la [**légende**](caption-property.md) des objets [**Commands**](/windows/desktop/lwef/the-commands-collection-object) du client. Cela vous permet de les éliminer de la grammaire active actuelle de votre client. Toutefois, étant donné que cela bloque potentiellement l’accès vocal à d’autres clients, réinitialisez cette propriété sur **true** après avoir traité l’entrée vocale de l’utilisateur.

La désactivation de la propriété n’affecte pas le menu contextuel du caractère. Les commandes globales ajoutées par le serveur s’affichent toujours. Vous ne pouvez pas les supprimer du menu contextuel.

 

