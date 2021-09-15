---
title: Propriété Status
description: Propriété Status
ms.assetid: vs|msagent|~\pacontrol_8xd6.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402e88185e1024aa5958d06936a6529ae4012622
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411510"
---
# <a name="status-property"></a>Propriété Status

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne l’état du canal de sortie audio.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent * * *. AudioOutput. Status**



| Valeur | Description                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------|
| 0     | Le canal de sortie audio est disponible (inoccupé).                                                                 |
| 1     | Il n’existe pas de prise en charge de la sortie audio. par exemple, parce qu’il n’y a pas de carte audio.                                |
| 2     | Impossible d’ouvrir le canal de sortie audio (est occupé). par exemple, parce qu’une autre application est en train de diffuser du contenu audio. |
| 3     | Le canal de sortie audio est occupé car le serveur traite l’entrée vocale de l’utilisateur.                              |
| 4     | Le canal de sortie audio est occupé car un caractère est actuellement en cours de discours.                                       |
| 5     | Le canal de sortie audio n’est pas occupé, mais il attend une entrée vocale de l’utilisateur.                                    |
| 6     | Un autre problème (inconnu) s’est produit lors de la tentative d’accès au canal de sortie audio.                          |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Ce paramètre permet à votre application cliente d’interroger le canal de sortie audio, en retournant une valeur entière qui indique l’état du canal de sortie audio. Vous pouvez l’utiliser pour déterminer s’il est approprié d’avoir votre caractère parlant ou s’il est approprié d’essayer d’activer le mode d’écoute (à l’aide de la méthode [**Listen**](listen-method.md) ).

## <a name="see-also"></a>Voir aussi

[**Événement ListenComplete**](listencomplete-event.md)


 

 




