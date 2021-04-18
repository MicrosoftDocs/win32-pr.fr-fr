---
description: Le Registre est une base de données hiérarchique qui contient des données qui sont essentielles au fonctionnement de Windows et aux applications et services qui s’exécutent sur Windows.
ms.assetid: 4ed60563-73d8-4134-8cb2-8388734fb18d
title: Structure du Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b76b7f827ae3ea96d75d089c7d874c3d31d030
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104554156"
---
# <a name="structure-of-the-registry"></a>Structure du Registre

Le Registre est une base de données hiérarchique qui contient des données qui sont essentielles au fonctionnement de Windows et aux applications et services qui s’exécutent sur Windows. Les données sont structurées dans un format d’arborescence. Chaque nœud de l’arborescence est appelé une *clé*. Chaque clé peut contenir à la fois des *sous-clés* et des entrées de données appelées *valeurs*. Parfois, la présence d’une clé correspond à toutes les données requises par une application. dans d’autres cas, une application ouvre une clé et utilise les valeurs associées à la clé. Une clé peut avoir n’importe quel nombre de valeurs, et les valeurs peuvent se présenter sous n’importe quelle forme. Pour plus d’informations, consultez [types de valeurs de Registre](registry-value-types.md) et limites de taille des [éléments du registre](registry-element-size-limits.md).

Chaque clé a un nom constitué d’un ou de plusieurs caractères imprimables. Les noms de clés ne respectent pas la casse. Les noms de clés ne peuvent pas contenir de barre oblique inverse ( \) , mais tout autre caractère imprimable peut être utilisé. Les noms de valeur et les données peuvent inclure une barre oblique inverse.

Le nom de chaque sous-clé est unique en ce qui concerne la clé qui est immédiatement au-dessus de celle-ci dans la hiérarchie. Les noms de clés ne sont pas localisés dans d’autres langues, bien que les valeurs puissent être.

L’illustration suivante est un exemple de structure de clé de registre telle qu’elle est affichée par l’éditeur du Registre.

![fenêtre de l’éditeur du Registre](images/regtree.png)

Chaque arborescence sous **poste de travail** est une clé. La clé de l' **\_ \_ ordinateur local HKEY** possède les sous-clés suivantes : **Hardware**, **Sam**, **Security**, **Software** et **System**. Chacune de ces clés a des sous-clés. Par exemple, la clé **matérielle** a les sous-clés **Description**, **DEVICEMAP** et **RESOURCEMAP**; la clé **DEVICEMAP** a plusieurs sous-clés, y compris la **vidéo**.

Chaque valeur se compose d’un nom de valeur et de ses données associées, le cas échéant. **MaxObjectNumber** et **VgaCompatible** sont des valeurs qui contiennent des données sous la sous-clé **Video** .

Une arborescence du Registre peut avoir 512 niveaux de profondeur. Vous pouvez créer jusqu’à 32 niveaux à la fois à l’aide d’un appel d’API de Registre unique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble du Registre Windows](/previous-versions/windows/it-pro/windows-server-2003/cc781906(v=ws.10))
</dt> </dl>

 

 
