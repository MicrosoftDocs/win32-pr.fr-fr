---
description: ICE44 vérifie que NewDialog, SpawnDialog et SpawnWaitDialog ControlEvents font référence à des boîtes de dialogue valides dans la table Dialog.
ms.assetid: 401bae25-a361-45f6-af3f-0f31be463c84
title: ICE44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ee7bb074ec2dcc395cdf17750e2ab1b0364026e0f949c9b9e3f2589a8b59261
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581009"
---
# <a name="ice44"></a>ICE44

ICE44 vérifie que [NewDialog](newdialog-controlevent.md), [SpawnDialog](spawndialog-controlevent.md)et [SpawnWaitDialog](spawnwaitdialog-controlevent.md) ControlEvents font référence à des boîtes de dialogue valides dans la [table Dialog](dialog-table.md).

## <a name="result"></a>Résultat

ICE44 publie un message d’erreur s’il existe un événement de contrôle de boîte de dialogue qui ne fait pas référence à une boîte de dialogue figurant dans la table de boîte de dialogue.

## <a name="example"></a>Exemples

ICE44 signale les erreurs suivantes pour l’exemple indiqué.



| Erreur ICE44                                                                                                                               | Description                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Événement de contrôle pour le contrôle’dialog1 '. ' Control1 'est de type SpawnDialog, mais son argument Dialog2 n’est pas une entrée valide dans la table Dialog. | Il existe une action SpawnDialog, SpawnWaitDialog ou NewDialog avec un argument qui ne fait pas référence à une boîte de dialogue dans la table Dialog. Pour corriger cette erreur, ajoutez un argument qui est une clé dans la table de boîte de dialogue.<br/> |



 

[Table de boîtes de dialogue](dialog-table.md) (partielle)



| Boîte de dialogue  | Titre |
|---------|-------|
| Dialog1 |       |



 

[Table ControlEvent,](controlevent-table.md) (partielle)



| Boîte de dialogue\_ | contrôle\_ | Type        | Argument |
|----------|-----------|-------------|----------|
| Dialog1  | Control1  | SpawnDialog | Dialog2  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 




