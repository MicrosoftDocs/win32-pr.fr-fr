---
description: ICE29 vérifie que les noms de flux tronqués restent uniques. Toute table ayant une colonne binaire ou objet est validée. Consultez le type de données de la colonne binaire.
ms.assetid: a51b641d-992b-4b6b-a208-d94bc7d05115
title: ICE29
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcdef203e314a087e9eb11bcf1b958425d7608028d979db925edce1b42e4bebc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528709"
---
# <a name="ice29"></a>ICE29

ICE29 vérifie que les noms de flux tronqués restent uniques. Toute table ayant une colonne binaire ou objet est validée. Consultez le type de données de la colonne [binaire](binary.md) .

La gestion des flux par l’implémentation de stockage structuré OLE Win32 limite les noms de flux. Consultez [restrictions OLE sur flux](ole-limitations-on-streams.md). Le programme d’installation peut compresser des noms de flux d’une longueur maximale de 62 caractères. Les noms plus longs sont tronqués.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



