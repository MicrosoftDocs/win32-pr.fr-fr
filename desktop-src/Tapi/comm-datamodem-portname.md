---
description: La classe d’appareil comm/datamodem/PortName se compose des noms des appareils auxquels les modems sont attachés.
ms.assetid: 174519f6-3e73-4f05-9718-9e38680a0fb7
title: comm/datamodem/PortName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f926dc87a093f49d41256b003e47c048caa5ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866921"
---
# <a name="commdatamodemportname"></a>comm/datamodem/PortName

La classe d’appareil comm/datamodem/PortName se compose des noms des appareils auxquels les modems sont attachés. Lorsque ce nom de périphérique est spécifié dans un appel à la fonction [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) , la fonction remplit la structure [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) avec une chaîne ANSI (non Unicode) terminée par un caractère null qui spécifie le nom du port auquel le modem spécifié est attaché, par exemple « COM1 \\ 0 ». Cela est principalement destiné à des fins d’identification dans l’interface utilisateur, mais peut être utilisé dans certaines circonstances pour ouvrir l’appareil directement, en ignorant le fournisseur de services (si l’appareil n’est pas déjà ouvert par le fournisseur de services). Si aucun port n’est associé à l’appareil, une chaîne null (« \\ 0 ») est retournée dans la structure **VARSTRING** (avec une longueur de chaîne de 1).

 

 



