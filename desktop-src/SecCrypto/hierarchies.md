---
description: Les services de certificats prennent en charge les hiérarchies d’autorité de certification.
ms.assetid: bcae26cd-41bc-4436-8f8b-cd8c20e9fcfc
title: Hiérarchies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1fe484d752fc7efc7f098aa1cd1af34d88e799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522144"
---
# <a name="hierarchies"></a>Hiérarchies

Les services de certificats prennent en charge les hiérarchies d' [*autorité de certification*](../secgloss/c-gly.md) . Une [*hiérarchie d’autorité de certification*](../secgloss/c-gly.md) se compose d’une autorité de certification de niveau supérieur (appelée autorité de certification racine) avec une ou plusieurs autorités de certification secondaires pour lesquelles des certificats ont été émis par l’autorité de certification racine. Un scénario de hiérarchie d’autorité de certification possible se trouve dans une organisation avec une autorité de certification racine, qui a été utilisée pour émettre des certificats pour plusieurs autorités de certification secondaires. Les autorités de certification secondaires peuvent ensuite émettre des certificats d’entité finale, tels que des certificats émis pour un utilisateur. Le certificat de l’utilisateur contient un chemin d’approbation pour la hiérarchie d’autorité de certification, dans ce cas, y compris le certificat pour l’autorité de certification secondaire émettrice, ainsi que pour l’autorité de certification racine.

 

 
