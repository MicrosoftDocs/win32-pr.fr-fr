---
description: Lorsque vous utilisez les infrastructures de représentation graphique d’homologue ou de regroupement d’homologues, les informations (enregistrements) que les homologues publient sur un graphique ou un groupe sont stockées en tant que base de données sur chaque ordinateur homologue.
ms.assetid: 1412b2eb-c97d-4415-998c-5f21eaadcc66
title: Importation et exportation de base de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc047e6f58c7aeab07f6d13f8f7364f3f2f1191e50320513bc153e34c4c042c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979059"
---
# <a name="database-import-and-export"></a>Importation et exportation de base de données

Lorsque vous utilisez les infrastructures de représentation graphique d’homologue ou de regroupement d’homologues, les informations (enregistrements) que les homologues publient sur un graphique ou un groupe sont stockées en tant que base de données sur chaque ordinateur homologue. Pour migrer une application d’un ordinateur à un autre, vous pouvez exporter une base de données de représentation graphique ou de regroupement d’homologues à partir d’un ordinateur, puis l’importer vers une autre.

La liste suivante identifie les informations importantes sur l’utilisation des bases de données :

-   Vous pouvez uniquement importer une base de données qui a le même graphique et l’ID homologue.
-   Vous ne pouvez pas appeler les fonctions d’importation et d’exportation si [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten), [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)ou [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) ont été appelés.

L' **infrastructure de représentation graphique des pairs** utilise les appels suivants pour importer et exporter une base de données d’enregistrement :

-   [**PeerGraphExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphexportdatabase)
-   [**PeerGraphImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphimportdatabase)

L' **infrastructure de regroupement de pairs** utilise les appels suivants pour importer et exporter une base de données d’enregistrement :

-   [**PeerGroupExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase)
-   [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase)

 

 



