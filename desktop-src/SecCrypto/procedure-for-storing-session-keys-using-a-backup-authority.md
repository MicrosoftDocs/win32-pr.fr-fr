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
# <a name="storing-session-keys-using-a-backup-authority"></a><span data-ttu-id="84bb6-103">Stockage des clés de session à l’aide d’une autorité de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="84bb6-103">Storing Session Keys Using a Backup Authority</span></span>

<span data-ttu-id="84bb6-104">Une application qui utilise une [*autorité de sauvegarde*](../secgloss/b-gly.md) pour stocker les clés de session suit généralement ces étapes.</span><span class="sxs-lookup"><span data-stu-id="84bb6-104">An application using a [*backup authority*](../secgloss/b-gly.md) to store session keys typically follows these steps.</span></span>

<span data-ttu-id="84bb6-105">**Pour utiliser une autorité de sauvegarde**</span><span class="sxs-lookup"><span data-stu-id="84bb6-105">**To use a backup authority**</span></span>

1.  <span data-ttu-id="84bb6-106">Chiffrez le fichier comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="84bb6-106">Encrypt the file as usual.</span></span>
2.  <span data-ttu-id="84bb6-107">Exportez la [*clé de session*](../secgloss/s-gly.md) utilisée pour chiffrer le fichier dans un [*objet blob de clé simple*](../secgloss/s-gly.md), en spécifiant que votre propre [*clé publique d’échange de clé*](../secgloss/k-gly.md) doit être utilisée pour chiffrer l’objet blob de clé.</span><span class="sxs-lookup"><span data-stu-id="84bb6-107">Export the [*session key*](../secgloss/s-gly.md) used to encrypt the file into a [*simple key BLOB*](../secgloss/s-gly.md), specifying that your own [*key exchange public key*](../secgloss/k-gly.md) be used to encrypt the key BLOB.</span></span> <span data-ttu-id="84bb6-108">Stockez cet objet BLOB de clé avec le fichier chiffré.</span><span class="sxs-lookup"><span data-stu-id="84bb6-108">Store this key BLOB with the encrypted file.</span></span>
3.  <span data-ttu-id="84bb6-109">Exportez de nouveau la clé de session, en spécifiant cette fois la clé publique de l’autorité de sauvegarde à utiliser pour chiffrer l’objet BLOB de clé.</span><span class="sxs-lookup"><span data-stu-id="84bb6-109">Export the session key again, this time specifying that the backup authority's public key be used to encrypt the key BLOB.</span></span> <span data-ttu-id="84bb6-110">Envoyez cet objet BLOB de clé à l’autorité de sauvegarde, ainsi que la description, le numéro de série et ainsi de suite de la clé.</span><span class="sxs-lookup"><span data-stu-id="84bb6-110">Send this key BLOB to the backup authority, along with the key's description, serial number, and so on.</span></span>

<span data-ttu-id="84bb6-111">Si une [*paire*](../secgloss/k-gly.md) de clés est perdue, les clés peuvent être récupérées à partir de l' [*autorité de sauvegarde*](../secgloss/b-gly.md) si l’identité du propriétaire de la clé peut être établie.</span><span class="sxs-lookup"><span data-stu-id="84bb6-111">If a [*key pair*](../secgloss/k-gly.md) is lost, the keys can be retrieved from the [*backup authority*](../secgloss/b-gly.md) if the identity of the keys' owner can be established.</span></span> <span data-ttu-id="84bb6-112">La procédure d’établissement de l’identité est déterminée par la stratégie de l’autorité de sauvegarde particulière et n’implique pas CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="84bb6-112">The procedure for establishing identity is determined by the policy of the particular backup authority and does not involve CryptoAPI.</span></span>

<span data-ttu-id="84bb6-113">Pour obtenir le code nécessaire à la création d’une clé de session et à l’exportation de cette clé vers un [*objet blob de clé simple*](../secgloss/s-gly.md) pouvant être écrit dans un fichier sur disque, consultez [exemple de programme C : exportation d’une clé de session](example-c-program-exporting-a-session-key.md).</span><span class="sxs-lookup"><span data-stu-id="84bb6-113">For the code needed to create a session key and export that key to a [*simple key BLOB*](../secgloss/s-gly.md) that can be written to a disk file, see [Example C Program: Exporting a Session Key](example-c-program-exporting-a-session-key.md).</span></span>

 

 
