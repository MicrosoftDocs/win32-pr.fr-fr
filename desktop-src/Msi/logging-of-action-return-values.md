---
description: Le programme d’installation écrit les valeurs suivantes dans le journal lorsqu’une action retourne ces codes d’erreur. pour obtenir la liste complète des codes d’erreur retournés par la fonction Windows Installer appelle MsiExec.exe et InstMsi.exe, consultez codes d’erreur.
ms.assetid: 653bbf45-ac2c-4f8a-a978-960e0c42e6e4
title: Journalisation des valeurs de retour d’action
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaaa203fee1fbb02bef070d065a9838383ea588b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021373"
---
# <a name="logging-of-action-return-values"></a>Journalisation des valeurs de retour d’action

Le programme d’installation écrit les valeurs suivantes dans le journal lorsqu’une action retourne ces codes d’erreur. pour obtenir la liste complète des codes d’erreur retournés par la fonction Windows Installer appelle MsiExec.exe et InstMsi.exe, consultez [codes d’erreur](error-codes.md).



| Code d'erreur                       | Les valeurs retournées par les appels de fonction MsiExec.exe et InstMsi.exe | Valeurs qui s’affichent dans le journal. | Description                                                                                                                                                                                                                                                                     |
|----------------------------------|----------------------------------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fonction d’erreur \_ \_ non \_ appelée     | 1626                                                           | 0                              | Une fonction n’a pas pu être exécutée.                                                                                                                                                                                                                                               |
| ERREUR de \_ réussite                   | 0                                                              | 1                              | Une action s’est terminée avec succès.                                                                                                                                                                                                                                               |
| ERREUR lors de l' \_ installation de \_ USEREXIT         | 1602                                                           | 2                              | L’utilisateur A annulé l’installation.                                                                                                                                                                                                                                                   |
| ERREUR d' \_ installation \_          | 1603                                                           | 3                              | Erreur irrécupérable.                                                                                                                                                                                                                                                                  |
| ERREUR d' \_ installation d' \_ interruption          | 1604                                                           | 4                              | L’installation a été interrompue, incomplète.                                                                                                                                                                                                                                         |
| ERREUR de \_ réussite                   | 0                                                              | 5                              | L’action s’est terminée avec succès.                                                                                                                                                                                                                                              |
| ERREUR \_ d' \_ État de handle non valide \_    | 1609                                                           | 6                              | Le descripteur est dans un État non valide.                                                                                                                                                                                                                                              |
| ERREUR de \_ données non valides \_             | 1626                                                           | 7                              | Les données ne sont pas valides.                                                                                                                                                                                                                                                            |
| ERREUR d' \_ installation \_ déjà \_ en cours d’exécution | 1618                                                           | 8                              | Une autre installation est en cours d’exécution. Une seule installation à la fois peut exécuter des actions dans les tables [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md)ou [AdvtExecuteSequence](advtexecutesequence-table.md) . |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Journalisation du programme d’installation](windows-installer-logging.md)
</dt> </dl>

 

 



