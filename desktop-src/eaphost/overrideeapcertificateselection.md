---
title: OverrideEAPCertificateSelection
description: La clé de Registre OverrideEAPCertificateSelection détermine si le client remplacera le comportement de sélection de certificat de carte à puce par défaut et fournira à l’utilisateur plus de certificats à choisir.
ms.assetid: 469FECA9-FF2A-46B1-9370-0FF28EF2FB33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d958eeeffba96e7a060ee4dd3edaf8a9935a15d1
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "103841741"
---
# <a name="overrideeapcertificateselection"></a>OverrideEAPCertificateSelection

La clé de Registre OverrideEAPCertificateSelection détermine si le client remplacera le comportement de sélection de certificat de carte à puce par défaut et fournira à l’utilisateur plus de certificats à choisir.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   OverrideEAPCertificateSelection = value
```

## <a name="remarks"></a>Notes

Il s’agit d’une valeur **\_ binaire de Reg** .



| Valeur | Description                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x000 | Ne substituez pas le comportement par défaut.                                                                                                                                                                |
| 0x001 | Choisissez le dernier certificat attaché à partir de la carte à puce.                                                                                                                                            |
| 0x010 | Affiche tous les certificats dans l’interface utilisateur de sélection de certificat à partir de la carte à puce.                                                                                                                          |
| 0x100 | Affiche tous les certificats de l’interface utilisateur de sélection de certificat à partir du Registre.                                                                                                                            |
| 0x101 | Affiche tous les certificats de l’interface utilisateur de sélection de certificat à partir du Registre et le dernier certificat attaché à la carte à puce. Affiche le dernier certificat attaché à partir de la carte à puce comme sélectionné. |
| 0x110 | Affiche tous les certificats de l’interface utilisateur de sélection de certificat à partir du Registre et de la carte à puce.                                                                                                         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Paramètres du Registre EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




