---
description: Une application qui utilise une autorité de sauvegarde pour stocker les clés de session suit généralement ces étapes.
ms.assetid: 859310ed-6000-44c8-92f7-974326ce0fc9
title: Stockage des clés de session à l’aide d’une autorité de sauvegarde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59906874f384d4eed9e20d6a781b14e3feba313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319266"
---
# <a name="storing-session-keys-using-a-backup-authority"></a>Stockage des clés de session à l’aide d’une autorité de sauvegarde

Une application qui utilise une [*autorité de sauvegarde*](../secgloss/b-gly.md) pour stocker les clés de session suit généralement ces étapes.

**Pour utiliser une autorité de sauvegarde**

1.  Chiffrez le fichier comme d’habitude.
2.  Exportez la [*clé de session*](../secgloss/s-gly.md) utilisée pour chiffrer le fichier dans un [*objet blob de clé simple*](../secgloss/s-gly.md), en spécifiant que votre propre [*clé publique d’échange de clé*](../secgloss/k-gly.md) doit être utilisée pour chiffrer l’objet blob de clé. Stockez cet objet BLOB de clé avec le fichier chiffré.
3.  Exportez de nouveau la clé de session, en spécifiant cette fois la clé publique de l’autorité de sauvegarde à utiliser pour chiffrer l’objet BLOB de clé. Envoyez cet objet BLOB de clé à l’autorité de sauvegarde, ainsi que la description, le numéro de série et ainsi de suite de la clé.

Si une [*paire*](../secgloss/k-gly.md) de clés est perdue, les clés peuvent être récupérées à partir de l' [*autorité de sauvegarde*](../secgloss/b-gly.md) si l’identité du propriétaire de la clé peut être établie. La procédure d’établissement de l’identité est déterminée par la stratégie de l’autorité de sauvegarde particulière et n’implique pas CryptoAPI.

Pour obtenir le code nécessaire à la création d’une clé de session et à l’exportation de cette clé vers un [*objet blob de clé simple*](../secgloss/s-gly.md) pouvant être écrit dans un fichier sur disque, consultez [exemple de programme C : exportation d’une clé de session](example-c-program-exporting-a-session-key.md).

 

 
