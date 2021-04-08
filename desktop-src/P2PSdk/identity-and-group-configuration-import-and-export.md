---
description: Les fichiers de configuration des identités et des groupes peuvent être importés et exportés d’un point de terminaison à un autre à l’aide des fonctions d’importation et d’exportation d’identité situées dans le gestionnaire d’identité et les API de regroupement.
ms.assetid: 876d9c57-15f6-4f5e-8035-792e15f8035e
title: Importation et exportation de la configuration d’identité et de groupe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a356f2747e3c8276446568b6f82bcbd773b14af8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756603"
---
# <a name="identity-and-group-configuration-import-and-export"></a><span data-ttu-id="3b53f-103">Importation et exportation de la configuration d’identité et de groupe</span><span class="sxs-lookup"><span data-stu-id="3b53f-103">Identity and Group Configuration Import and Export</span></span>

<span data-ttu-id="3b53f-104">Les fichiers de configuration des identités et des groupes peuvent être importés et exportés d’un point de terminaison à un autre à l’aide des fonctions d’importation et d’exportation d’identité situées dans le gestionnaire d’identité et les API de regroupement.</span><span class="sxs-lookup"><span data-stu-id="3b53f-104">Peer identity and group configuration files can be imported and exported from one endpoint to another by using the identity import and export functions located in the Identity Manager and Grouping APIs.</span></span> <span data-ttu-id="3b53f-105">Ces fonctions sont utiles car elles permettent à un utilisateur d’exporter rapidement et facilement des identités et des informations de configuration de groupe d’un ordinateur vers un autre.</span><span class="sxs-lookup"><span data-stu-id="3b53f-105">These functions are useful because they allow a user to quickly and conveniently export identities and group configuration information from one computer to another computer.</span></span>

## <a name="importing-and-exporting-peer-identity-data"></a><span data-ttu-id="3b53f-106">Importation et exportation des données d’identité de l’homologue</span><span class="sxs-lookup"><span data-stu-id="3b53f-106">Importing and Exporting Peer Identity Data</span></span>

<span data-ttu-id="3b53f-107">Les données d’identité d’un homologue sont exportées en appelant [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport) avec le nom d’identité à exporter et un mot de passe utilisé pour chiffrer les informations d’identification associées.</span><span class="sxs-lookup"><span data-stu-id="3b53f-107">The identity data of a peer is exported by calling [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport) with the identity name to export and a password used to encrypt the associated credentials.</span></span> <span data-ttu-id="3b53f-108">Cette fonction retourne une chaîne XML qui contient le nom d’identité de l’homologue et les informations d’identification chiffrées pour cette identité spécifique, qui peuvent ensuite être passées à un autre ordinateur à l’aide d’un mécanisme de transfert externe, tel que le courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="3b53f-108">This function returns an XML string that contains the identity name of the peer and the encrypted credentials for that specific identity, which can then be passed to a different computer by using an external transfer mechanism, such as e-mail.</span></span> <span data-ttu-id="3b53f-109">L’exemple suivant montre le format de la chaîne XML :</span><span class="sxs-lookup"><span data-stu-id="3b53f-109">The following example shows you the format of the XML string:</span></span>

``` syntax
<PEERIDENTITYEXPORT VERSION="1.0">
   <PEERNAME>
     <!-- UTF-8 encoded peer name of the identity -->
   </PEERNAME>
   <DATA xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
      <!-- base64 encoded / PFX encoded and encrypted IDC with the private key -->
   </DATA>
</PEERIDENTITYEXPORT>
```

<span data-ttu-id="3b53f-110">Les données d’identité exportées peuvent être récupérées en appelant [**PeerIdentityImport**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport)et en passant la chaîne XML avec le mot de passe fourni lors de l’appel précédent à [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport).</span><span class="sxs-lookup"><span data-stu-id="3b53f-110">The exported identity data can be retrieved by calling [**PeerIdentityImport**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport), and passing in the XML string with the password supplied in the previous call to [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport).</span></span> <span data-ttu-id="3b53f-111">Cette fonction retourne le nom d’homologue de l’identité importée.</span><span class="sxs-lookup"><span data-stu-id="3b53f-111">This function returns the peer name of the imported identity.</span></span> <span data-ttu-id="3b53f-112">Le nom d’identité et les informations d’identification importés peuvent être utilisés comme un nom d’identité retourné par [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) ou [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).</span><span class="sxs-lookup"><span data-stu-id="3b53f-112">The imported identity name and credentials can be used just like an identity name returned by [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) or [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).</span></span>

> [!Note]  
> <span data-ttu-id="3b53f-113">Lors de l’appel de [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport), l’application ou l’utilisateur de l’API doit fournir un mot de passe fort d’une longueur suffisante.</span><span class="sxs-lookup"><span data-stu-id="3b53f-113">When calling [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport), the application or API user must provide a strong password of sufficient length.</span></span> <span data-ttu-id="3b53f-114">Cela est important, car les données d’identité importées contiennent la clé privée pour l’identité.</span><span class="sxs-lookup"><span data-stu-id="3b53f-114">This is important because the imported identity data contains the private key for the identity.</span></span>

 

## <a name="importing-and-exporting-a-group-identity-configuration"></a><span data-ttu-id="3b53f-115">Importation et exportation d’une configuration d’identité de groupe</span><span class="sxs-lookup"><span data-stu-id="3b53f-115">Importing and Exporting a Group Identity Configuration</span></span>

<span data-ttu-id="3b53f-116">Le regroupement de pairs permet à un homologue d’exporter des données de configuration de groupe d’un point de terminaison à un autre à l’aide d’API d’importation et d’exportation spécifiques.</span><span class="sxs-lookup"><span data-stu-id="3b53f-116">Peer Grouping allows a peer to export group configuration data from one endpoint to another by using specific import and export APIs.</span></span> <span data-ttu-id="3b53f-117">Pour importer des données de configuration, l’identité de l’homologue effectuant l’importation (et qui a effectué précédemment l’exportation) doit être présente sur l’ordinateur sur lequel les données de configuration doivent être importées.</span><span class="sxs-lookup"><span data-stu-id="3b53f-117">To import configuration data, the identity of the peer performing the import (and who previously performed the export) must be present on the computer where the configuration data is to be imported.</span></span> <span data-ttu-id="3b53f-118">Cette identité peut être obtenue en l’exportant et en l’important par les méthodes spécifiées dans la section précédente de cette rubrique : [importation et exportation de données d’identité homologue](#importing-and-exporting-peer-identity-data).</span><span class="sxs-lookup"><span data-stu-id="3b53f-118">This identity can be obtained by exporting and importing it by the methods specified in the previous section of this topic: [Importing and Exporting Peer Identity Data](#importing-and-exporting-peer-identity-data).</span></span>

<span data-ttu-id="3b53f-119">Les données de configuration de groupe contiennent toutes les informations d’une identité pour joindre un groupe à partir d’un nouveau point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="3b53f-119">The group configuration data contains all of the information for an identity to join a group from a new endpoint.</span></span> <span data-ttu-id="3b53f-120">Plus précisément, les données de configuration contiennent la chaîne GMC, le nom d’homologue du groupe, le nom du Cloud, l’étendue et un ensemble d’indicateurs spécifiques à PNRP.</span><span class="sxs-lookup"><span data-stu-id="3b53f-120">Specifically, the configuration data contains the GMC chain, group peer name, cloud name, scope, and a set of PNRP specific flags.</span></span> <span data-ttu-id="3b53f-121">Pour une identité qui possède un groupe, une clé privée pour le groupe est incluse dans les informations de configuration du groupe.</span><span class="sxs-lookup"><span data-stu-id="3b53f-121">For an identity that owns a group, a private key for the group is included in the group configuration information.</span></span>

> [!Note]  
> <span data-ttu-id="3b53f-122">Lors de l’appel de [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), une application ou un utilisateur d’API doit fournir un mot de passe fort d’une longueur suffisante.</span><span class="sxs-lookup"><span data-stu-id="3b53f-122">When calling [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), an application or API user must provide a strong password of sufficient length.</span></span> <span data-ttu-id="3b53f-123">Cela est important, car les données d’identité importées contiennent la clé privée pour le groupe.</span><span class="sxs-lookup"><span data-stu-id="3b53f-123">This is important because the imported identity data contains the private key for the group.</span></span>

 

<span data-ttu-id="3b53f-124">Pour exporter la configuration actuelle du groupe homologue, appelez [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), en passant le handle au groupe (obtenu par un appel précédent à [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)ou [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)) et un mot de passe utilisé pour chiffrer et protéger le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="3b53f-124">To export the current peer group configuration, call [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), passing in the handle to the group (obtained by a previous call to [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen), or [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)), and a password used to encrypt and protect the configuration file.</span></span> <span data-ttu-id="3b53f-125">Cette fonction retourne une chaîne XML qui contient la configuration dans le format de l’exemple suivant, qui peut ensuite être écrit dans un fichier et transmis à un autre ordinateur à l’aide d’un mécanisme de transfert externe, tel que la messagerie électronique.</span><span class="sxs-lookup"><span data-stu-id="3b53f-125">This function returns an XML string that contains the configuration in the format of the following example, which can then be written to a file and passed to another computer by using an external transfer mechanism, such as email.</span></span>

``` syntax
<PEERGROUPCONFIG VERSION="1.0">
  <IDENTITYPEERNAME>
    <!-- UTF-8 encoded peer name of the identity -->
  </IDENTITYPEERNAME>
  <GROUPPEERNAME>
    <!-- UTF-8 encoded peer name of the group -->
  </GROUPPEERNAME>
  <CLOUDNAME>
    <!-- UTF-8 encoded Unicode name of the cloud -->
  </CLOUDNAME>
  <SCOPE>
    <!-- UTF-8 encoded Unicode name of the scope: global, site-local, link-local -->
  </SCOPE>
  <CLOUDFLAGS>
    <!-- A DWORD that contains cloud-specific settings, represented as a string -->
  </CLOUDFLAGS>
  <GMC xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
    <!-- base64/PKCS7 encoded GMC chain -->
  </GMC>
</PEERGROUPCONFIG>
```

<span data-ttu-id="3b53f-126">Après avoir obtenu la configuration de groupe sous la forme d’une chaîne XML, vous pouvez importer le groupe en appelant [**PeerGroupImportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) avec la chaîne de configuration XML et le mot de passe spécifique fourni à [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig).</span><span class="sxs-lookup"><span data-stu-id="3b53f-126">After obtaining the group configuration as an XML string, the group can be imported by calling [**PeerGroupImportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) with the configuration XML string and the specific password supplied to [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig).</span></span> <span data-ttu-id="3b53f-127">Cette fonction retourne un nom d’identité et un nom d’homologue de groupe, qui peuvent ensuite être fournis à [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) et une connexion au groupe établi.</span><span class="sxs-lookup"><span data-stu-id="3b53f-127">This function returns an identity name and a group peer name, which can then be supplied to [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) and a connection to the group established.</span></span>

 

 



