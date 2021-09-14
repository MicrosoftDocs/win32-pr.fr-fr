---
description: ICE29 vérifie que les noms de flux tronqués restent uniques. Toute table ayant une colonne binaire ou objet est validée. Consultez le type de données de la colonne binaire.
ms.assetid: a51b641d-992b-4b6b-a208-d94bc7d05115
title: ICE29
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f606bd09314d045b643816c08349eba38bde72
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021584"
---
# <a name="ice29"></a>ICE29

ICE29 vérifie que les noms de flux tronqués restent uniques. Toute table ayant une colonne binaire ou objet est validée. Consultez le type de données de la colonne [binaire](binary.md) .

La gestion des flux par l’implémentation de stockage structuré OLE Win32 limite les noms de flux. Consultez [restrictions OLE sur flux](ole-limitations-on-streams.md). Le programme d’installation peut compresser des noms de flux d’une longueur maximale de 62 caractères. Les noms plus longs sont tronqués.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



