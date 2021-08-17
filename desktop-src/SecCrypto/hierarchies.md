---
description: Les services de certificats prennent en charge les hiérarchies d’autorité de certification.
ms.assetid: bcae26cd-41bc-4436-8f8b-cd8c20e9fcfc
title: Hierarchies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 240f2f2fc2920db1a67adb18281ad5c1d67fabdb2996ae3aae8342f96b1810c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006297"
---
# <a name="hierarchies"></a>Hierarchies

Les services de certificats prennent en charge les hiérarchies d' [*autorité de certification*](../secgloss/c-gly.md) . Une [*hiérarchie d’autorité de certification*](../secgloss/c-gly.md) se compose d’une autorité de certification de niveau supérieur (appelée autorité de certification racine) avec une ou plusieurs autorités de certification secondaires pour lesquelles des certificats ont été émis par l’autorité de certification racine. Un scénario de hiérarchie d’autorité de certification possible se trouve dans une organisation avec une autorité de certification racine, qui a été utilisée pour émettre des certificats pour plusieurs autorités de certification secondaires. Les autorités de certification secondaires peuvent ensuite émettre des certificats d’entité finale, tels que des certificats émis pour un utilisateur. Le certificat de l’utilisateur contient un chemin d’approbation pour la hiérarchie d’autorité de certification, dans ce cas, y compris le certificat pour l’autorité de certification secondaire émettrice, ainsi que pour l’autorité de certification racine.

 

 
