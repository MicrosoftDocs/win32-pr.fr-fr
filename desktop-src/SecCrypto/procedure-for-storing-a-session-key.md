---
description: Explique la procédure utilisée pour stocker une clé de session.
ms.assetid: 9ab7f747-9c69-40b5-af78-163f3ba315bf
title: Stockage d’une clé de session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b17de657ddba47dd77f68c1ee7a2adfdf93e7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524681"
---
# <a name="storing-a-session-key"></a>Stockage d’une clé de session

> [!Note]  
> Cette section part du principe que les utilisateurs possèdent un ensemble de [*paires de clés publiques/privées*](../secgloss/p-gly.md). Vous trouverez des instructions et un exemple de création de paires de clés dans l' [exemple de programme C : création d’un conteneur de clé et génération de clés](example-c-program-creating-a-key-container-and-generating-keys.md).

 

**Pour stocker une clé de session**

1.  Créez un [*objet blob de clé*](../secgloss/k-gly.md) simple à l’aide de la fonction [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) . Cela permet de transférer la clé de session du CSP vers l’espace mémoire d’une application. Spécifie qu’une clé publique Exchange doit être utilisée pour signer l’objet BLOB de clé.
2.  Stockez l’objet BLOB de clé signée sur le disque. Il est supposé que tous les disques sont non sécurisés.
3.  Lorsque la clé est nécessaire, lisez l’objet BLOB de clé à partir du disque.
4.  Importez à nouveau l’objet BLOB de clé dans le CSP à l’aide de la fonction [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) .

Pour obtenir un exemple de création d’une [*clé de session*](../secgloss/s-gly.md) et d’exportation de cette clé vers un [*objet blob de clé simple*](../secgloss/s-gly.md) pouvant être écrit dans un fichier sur disque, consultez [exemple de programme C : exportation d’une clé de session](example-c-program-exporting-a-session-key.md).

Cette procédure fournit uniquement une sécurité minimale. Si la clé de session stockée sera utilisée pour chiffrer les données à une date ultérieure, la procédure précédente ne fournit pas de sécurité adéquate.

Pour renforcer la sécurité, signez l’objet BLOB de clé avec une clé privée Exchange avant qu’il ne soit stocké sur le disque. Lorsque l’objet BLOB de clé est lu ultérieurement à partir du disque, sa signature peut être validée pour s’assurer que l’objet BLOB de clé est intact.

Si l’objet BLOB de clé n’est pas signé, toute personne ayant accès au disque ou à un autre support où la clé est stockée peut créer une nouvelle clé de session.

La nouvelle clé de session peut être chiffrée avec la [*clé d’échange*](../secgloss/e-gly.md)de [*clé publique*](../secgloss/p-gly.md) de l’utilisateur d’origine, et cette nouvelle clé peut être substituée à l’original. Si l’utilisateur a déjà utilisé la clé de session substituée pour chiffrer les fichiers et les messages, la personne qui a créé la clé de substitution peut facilement les déchiffrer.

Les signatures numériques sont décrites en détail dans [hachages et signatures numériques](hashes-and-digital-signatures.md).

 

 
