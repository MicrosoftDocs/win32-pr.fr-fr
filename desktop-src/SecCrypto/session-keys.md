---
description: Les clés de session sont des clés générées pour être utilisées dans une session de communication unique.
ms.assetid: 18bf2023-084d-400d-b60d-1ba51ce6a2bc
title: Clés de session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db4089f9ab5a0ae6889463c1b24c2eecb376c7f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535573"
---
# <a name="session-keys"></a>Clés de session

Les [*clés de session*](../secgloss/s-gly.md) sont des clés générées pour être utilisées dans une session de communication unique. Les clés de session sont fréquemment modifiées et sont ignorées lorsqu’elles ne sont plus nécessaires. Par exemple, TLS utilise une clé de session distincte pour chaque connexion et S/MIME utilise une clé de session distincte pour chaque message électronique. En général, une [*clé symétrique*](../secgloss/s-gly.md) est utilisée comme clé de session.

Les clés de session sont volatiles. Les applications peuvent enregistrer ces clés pour une utilisation ultérieure ou pour les transmettre à d’autres utilisateurs. Pour plus d’informations, consultez [stockage de clés de chiffrement et Exchange](cryptographic-key-storage-and-exchange.md).

 

 
