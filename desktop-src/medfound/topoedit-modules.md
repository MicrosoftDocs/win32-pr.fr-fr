---
description: Modules TopoEdit
ms.assetid: f3da2d13-a8ad-4db0-9d18-e94857f0abc7
title: Modules TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc95848a533ba67599c114917ebe502f42a4fe859df9c1ac6bf5acfc40bb393c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118057714"
---
# <a name="topoedit-modules"></a>Modules TopoEdit

l’outil TopoEdit est fourni avec la SDK Windows pour Windows Server 2008 et versions ultérieures. l’outil requiert Windows Vista ou version ultérieure.

Les modules TopoEdit se trouvent dans le dossier bin du kit de développement logiciel (SDK). Ces modules sont les suivants :

-   TopoEdit.exe : exécutable de l’application
-   TEDUTIL.dll : DLL d’extension

L’installation du kit de développement logiciel (SDK) inscrit la DLL. Toutefois, si cette opération échoue, à l’invite de commandes, exécutez la commande suivante.


```C++
Regsvr32 <Install path>\Microsoft SDKs\Windows\v6.0\Bin\TEDUTIL.dll
```



le code Source pour TopoEdit est également fourni sous la forme d’un exemple dans le SDK Windows. Il se trouve dans le répertoire suivant :

<samples root>\\\\TopoEdit multimédia Media Foundation \\

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Présentation de TopoEdit](introduction-to-topoedit.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



