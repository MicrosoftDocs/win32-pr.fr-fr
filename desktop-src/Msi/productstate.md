---
description: Le programme d’installation définit la propriété ProductState sur l’état d’installation du produit lors de l’initialisation.
ms.assetid: 833e9a15-10f8-4b1c-945f-bc02b506f627
title: Propriété ProductState
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88b4be53a1764d2277aec2b9acc50ae2a62ee7cb6687752466529c7ceabc689d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074659"
---
# <a name="productstate-property"></a>Propriété ProductState

Le programme d’installation définit la propriété **ProductState** sur l’état d’installation du produit lors de l’initialisation. Cette propriété est définie sur l’un des types de données INSTALLSTATE suivants retournés par [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea).



| INSTALLSTATE             | Valeur numérique | État d’installation du produit                   |
|--------------------------|---------------|-------------------------------------------------|
| INSTALLSTATE \_ inconnu    | -1            | Le produit n’est ni publié ni installé. |
| INSTALLSTATE \_ publié | 1             | Le produit est publié, mais n’est pas installé.    |
| INSTALLSTATE \_ absent     | 2             | Le produit est installé pour un autre utilisateur.  |
| INSTALLSTATE \_ par défaut    | 5             | Le produit est installé pour l’utilisateur actuel.  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




