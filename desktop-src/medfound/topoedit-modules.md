---
description: Modules TopoEdit
ms.assetid: f3da2d13-a8ad-4db0-9d18-e94857f0abc7
title: Modules TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728f39edace5974d390746173308361b595c3b40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296234"
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

 

 



