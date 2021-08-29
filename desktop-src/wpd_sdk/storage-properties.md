---
description: Windows Les appareils mobiles prennent en charge les propriétés de stockage suivantes.
ms.assetid: 234078c3-e703-41f3-9b18-ae61d8a36784
title: Stockage Propriétés (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Storage
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 0dbf88d02e59cca59e4bb3ee14ffd90c1741478f8b6a90ea296087388b9bb099
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806509"
---
# <a name="storage-properties"></a>Propriétés de stockage

Windows Les appareils mobiles prennent en charge les propriétés de stockage suivantes.



| Propriété                                   | VarType        | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_capacité de stockage wpd \_**                 | **\_UI8 VT**    | Capacité totale de stockage, en octets.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **\_ \_ capacité de stockage wpd dans les \_ \_ objets**    | **\_UI8 VT**    | Indique la capacité de stockage totale dans les objets ; par exemple, les emplacements disponibles sur une carte SIM.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **\_Description du stockage wpd \_**              | **\_LPWStr VT** | Description explicite du stockage.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **\_type de \_ système de fichiers de stockage wpd \_ \_**       | **\_LPWStr VT** | Description de chaîne du système de fichiers utilisé par le stockage, par exemple « FAT32 », « NTFS », « système de fichiers contoso », et ainsi de suite.                                                                                                                                                                                                                                                                                                                                                                                                         |
| **\_ \_ espace libre de stockage wpd \_ \_ en \_ octets**   | **\_UI8 VT**    | Espace de stockage disponible, en octets.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **\_ \_ espace libre de stockage wpd \_ dans les \_ \_ objets** | **\_UI8 VT**    | Nombre d’objets supplémentaires qui peuvent être écrits sur l’appareil. Par exemple, si un appareil n’autorise qu’un seul objet, il s’agit de zéro si l’objet existait déjà.                                                                                                                                                                                                                                                                                                                                                          |
| **\_numéro de \_ série du stockage wpd \_**           | **\_LPWStr VT** | Numéro de série spécifique au fournisseur pour le stockage.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **\_ \_ taille maximale d' \_ objet du stockage wpd \_**        | **\_UI8 VT**    | Spécifie la taille maximale, en octets, d’un seul objet pouvant être placé sur ce stockage.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **\_type de stockage wpd \_**                     | **VT \_ UI4**    | Décrit le type physique d’un support de stockage de mémoire.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **\_capacité d' \_ accès au stockage wpd \_**       | **VT \_ UI4**    | Identifie toute protection en écriture qui affecte globalement ce stockage. Cela est prioritaire par rapport à l’accès spécifié sur les objets individuels. Les valeurs possibles proviennent de l’énumération des **\_ valeurs de \_ \_ capacité \_ d’accès au stockage wpd** définie dans PortableDevice. h. Par exemple, si **le \_ \_ type de stockage wpd** est ROM (il s’agit du **type de \_ stockage wpd \_ \_ fixe \_** ou ROM amovible du **\_ type de stockage \_ \_ \_ wpd**), la valeur de la **\_ \_ \_ capacité d’accès au** stockage wpd doit être **fonction d' \_ \_ accès au stockage wpd \_ \_ lecture \_ seule \_ sans \_ \_ Suppression d’objet**. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés et attributs WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




