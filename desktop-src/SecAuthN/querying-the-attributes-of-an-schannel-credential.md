---
description: Fournit des informations spécifiques à Schannel sur les informations d’identification.
ms.assetid: 0c357996-b85a-4231-b258-40b35ab83ae2
title: Interrogation des attributs d’une information d’identification Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa940e6214f23a69af2e0f7de58813e007129caadac46be8a6c436b8d62094f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919908"
---
# <a name="querying-the-attributes-of-an-schannel-credential"></a>Interrogation des attributs d’une information d’identification Schannel

La fonction [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) fournit des informations spécifiques à Schannel sur les informations d’identification. Ces informations sont spécifiées à l’origine lors de la création des informations d’identification. Pour plus d’informations, consultez [obtention d’informations d’identification Schannel](obtaining-schannel-credentials.md). Les informations signalées par cette fonction sont valides pour toutes les connexions ([*contextes de sécurité*](../secgloss/s-gly.md)) créées à l’aide des informations d’identification spécifiées.

 

 
