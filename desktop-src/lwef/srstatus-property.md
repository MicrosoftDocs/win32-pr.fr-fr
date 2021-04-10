---
title: Propriété SRStatus
description: Propriété SRStatus
ms.assetid: 67618a35-05e4-4bb3-b910-c75de6e32578
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64cb6ba16bc024a52b65efa98c22fd089ad79da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029878"
---
# <a name="srstatus-property"></a>Propriété SRStatus

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne une valeur indiquant si l’entrée vocale peut être démarrée pour le caractère.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent. ***Caractères («*** CharacterID * * * »). SRStatus**



| Valeur | Description                                                                                                                                                                                                                               |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Les conditions prennent en charge l’entrée vocale.                                                                                                                                                                                                          |
| 1     | Aucun périphérique d’entrée audio n’est disponible sur ce système. (Notez que cela ne détecte pas si un microphone est installé ; il peut détecter uniquement si l’utilisateur dispose d’une carte son compatible avec un pilote opérationnel.) |
| 2     | Un autre client est le client actif de ce caractère, ou le caractère actuel n’est pas au premier plan.                                                                                                                                           |
| 3     | Le canal d’entrée ou de sortie audio est actuellement occupé, une application utilise l’audio.                                                                                                                                                       |
| 4     | Une erreur non spécifiée s’est produite lors de l’initialisation du sous-système de reconnaissance vocale. Cela inclut la possibilité qu’aucun moteur vocal ne soit disponible correspondant au paramètre de langue du caractère.                          |
| 5     | L’utilisateur a désactivé l’entrée vocale dans les options de caractères avancés.                                                                                                                                                                     |
| 6     | Une erreur s’est produite lors de la vérification de l’État audio, mais la cause de l’erreur n’a pas été retournée par le système.                                                                                                                                |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Cette propriété retourne les conditions nécessaires à la prise en charge de l’entrée vocale, y compris l’état du périphérique audio. Vous pouvez vérifier cette propriété avant d’appeler la méthode [**Listen**](listen-method.md) pour mieux garantir sa réussite.

Lorsque l’entrée vocale est activée dans la feuille de propriétés de l’agent (options de caractères avancés), l’interrogation de cette propriété chargera le moteur associé, s’il n’est pas déjà chargé, et démarrera les services de reconnaissance vocale. Autrement dit, la clé d’écoute est disponible et l’info-bulle d’écoute est automatiquement affichable. (La clé d’écoute et l’info-bulle d’écoute sont activées uniquement si elles sont également activées dans les options de caractères avancés.) Toutefois, si vous interrogez la propriété alors que la reconnaissance vocale est désactivée, le serveur ne démarre pas les services vocaux.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

## <a name="see-also"></a>Voir aussi

[**Méthode Listen**](listen-method.md)


 

 




