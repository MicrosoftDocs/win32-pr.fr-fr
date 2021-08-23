---
description: Les fichiers de configuration des identités et des groupes peuvent être importés et exportés d’un point de terminaison à un autre à l’aide des fonctions d’importation et d’exportation d’identité situées dans le gestionnaire d’identité et les API de regroupement.
ms.assetid: 876d9c57-15f6-4f5e-8035-792e15f8035e
title: Importation et exportation de la configuration d’identité et de groupe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0102bda821b7157edc512aeea4a8e315c0dbfa1def85f9a61919ec0f2c86da39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519329"
---
# <a name="identity-and-group-configuration-import-and-export"></a>Importation et exportation de la configuration d’identité et de groupe

Les fichiers de configuration des identités et des groupes peuvent être importés et exportés d’un point de terminaison à un autre à l’aide des fonctions d’importation et d’exportation d’identité situées dans le gestionnaire d’identité et les API de regroupement. Ces fonctions sont utiles car elles permettent à un utilisateur d’exporter rapidement et facilement des identités et des informations de configuration de groupe d’un ordinateur vers un autre.

## <a name="importing-and-exporting-peer-identity-data"></a>Importation et exportation des données d’identité de l’homologue

Les données d’identité d’un homologue sont exportées en appelant [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport) avec le nom d’identité à exporter et un mot de passe utilisé pour chiffrer les informations d’identification associées. Cette fonction retourne une chaîne XML qui contient le nom d’identité de l’homologue et les informations d’identification chiffrées pour cette identité spécifique, qui peuvent ensuite être passées à un autre ordinateur à l’aide d’un mécanisme de transfert externe, tel que le courrier électronique. L’exemple suivant montre le format de la chaîne XML :

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

Les données d’identité exportées peuvent être récupérées en appelant [**PeerIdentityImport**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport)et en passant la chaîne XML avec le mot de passe fourni lors de l’appel précédent à [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport). Cette fonction retourne le nom d’homologue de l’identité importée. Le nom d’identité et les informations d’identification importés peuvent être utilisés comme un nom d’identité retourné par [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) ou [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).

> [!Note]  
> Lors de l’appel de [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport), l’application ou l’utilisateur de l’API doit fournir un mot de passe fort d’une longueur suffisante. Cela est important, car les données d’identité importées contiennent la clé privée pour l’identité.

 

## <a name="importing-and-exporting-a-group-identity-configuration"></a>Importation et exportation d’une configuration d’identité de groupe

Le regroupement de pairs permet à un homologue d’exporter des données de configuration de groupe d’un point de terminaison à un autre à l’aide d’API d’importation et d’exportation spécifiques. Pour importer des données de configuration, l’identité de l’homologue effectuant l’importation (et qui a effectué précédemment l’exportation) doit être présente sur l’ordinateur sur lequel les données de configuration doivent être importées. Cette identité peut être obtenue en l’exportant et en l’important par les méthodes spécifiées dans la section précédente de cette rubrique : [importation et exportation de données d’identité homologue](#importing-and-exporting-peer-identity-data).

Les données de configuration de groupe contiennent toutes les informations d’une identité pour joindre un groupe à partir d’un nouveau point de terminaison. Plus précisément, les données de configuration contiennent la chaîne GMC, le nom d’homologue du groupe, le nom du Cloud, l’étendue et un ensemble d’indicateurs spécifiques à PNRP. Pour une identité qui possède un groupe, une clé privée pour le groupe est incluse dans les informations de configuration du groupe.

> [!Note]  
> Lors de l’appel de [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), une application ou un utilisateur d’API doit fournir un mot de passe fort d’une longueur suffisante. Cela est important, car les données d’identité importées contiennent la clé privée pour le groupe.

 

Pour exporter la configuration actuelle du groupe homologue, appelez [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), en passant le handle au groupe (obtenu par un appel précédent à [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)ou [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)) et un mot de passe utilisé pour chiffrer et protéger le fichier de configuration. Cette fonction retourne une chaîne XML qui contient la configuration dans le format de l’exemple suivant, qui peut ensuite être écrit dans un fichier et transmis à un autre ordinateur à l’aide d’un mécanisme de transfert externe, tel que la messagerie électronique.

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

Après avoir obtenu la configuration de groupe sous la forme d’une chaîne XML, vous pouvez importer le groupe en appelant [**PeerGroupImportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) avec la chaîne de configuration XML et le mot de passe spécifique fourni à [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig). Cette fonction retourne un nom d’identité et un nom d’homologue de groupe, qui peuvent ensuite être fournis à [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) et une connexion au groupe établi.

 

 



