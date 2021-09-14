---
description: Cette stratégie système par ordinateur est utilisée uniquement si la journalisation n’a pas été activée par l' &\# 0034 ;/l&\# 0034 ; option de ligne de commande ou par MsiEnableLog.
ms.assetid: d8649808-5dc3-4496-8c2f-da9b1512b5aa
title: journalisation (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a461051022791e414fe7e211e4dde33c7e83101b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021371"
---
# <a name="logging-windows-installer"></a>journalisation (Windows Installer)

Cette [stratégie système](system-policy.md) par ordinateur est utilisée uniquement si la journalisation n’a pas été activée par l’option de ligne de commande « /l » ou par [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga). Si la stratégie est définie dans ce cas, le programme d’installation crée un fichier journal dans% Temp% avec le nom aléatoire : MSI \* . Sign. Spécifiez le mode de journalisation en affectant une chaîne de caractères à la valeur de la stratégie. Utilisez les mêmes caractères pour spécifier la stratégie de mode de journalisation telle qu’elle est utilisée par l' [option de ligne de commande](command-line-options.md)« /l ». Notez que vous ne pouvez pas utiliser « + » et « \* » pour la stratégie.

Le mode de journalisation peut être défini à l’aide d’une stratégie, d’une option de ligne de commande ou par programme. pour plus d’informations sur toutes les méthodes qui sont disponibles pour définir le mode de journalisation, consultez [journalisation normale](normal-logging.md) dans la section [journalisation Windows Installer](windows-installer-logging.md) .

Vous pouvez empêcher que des informations confidentielles, par exemple des mots de passe, soient entrées dans le fichier journal et rendues visibles. Pour plus d’informations, consultez [empêcher l’écriture d’informations confidentielles dans le fichier journal](preventing-confidential-information-from-being-written-into-the-log-file.md) .

## <a name="registry-key"></a>Clé de Registre

Définissez la valeur nommée Logging sous la clé de Registre suivante.

**HKEY \_ \_** \\ **stratégies logicielles** de l’ordinateur LOCAL \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Type de données

**SZ de REG \_**

 

 



