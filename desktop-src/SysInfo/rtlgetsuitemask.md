---
description: Récupère un masque de bits qui identifie les suites de produits disponibles sur le système. Si cette fonction est appelée dans une application qui s’exécute dans le contexte d’un silo de serveurs, le masque de suite du silo de serveurs est récupéré à la place.
ms.assetid: 1D6434FD-D7BD-45F9-B7C3-238890AF9928
title: RtlGetSuiteMask, fonction (Ntddk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetSuiteMask
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: ed8d8906273d18125131251636bc6199d166547b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520645"
---
# <a name="rtlgetsuitemask-function"></a>RtlGetSuiteMask fonction)

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

Récupère un masque de bits qui identifie les suites de produits disponibles sur le système. Si cette fonction est appelée dans une application qui s’exécute dans le contexte d’un silo de serveurs, le masque de suite du silo de serveurs est récupéré à la place.

## <a name="syntax"></a>Syntaxe


```C++
ULONG NTAPI RtlGetSuiteMask(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Masque de bits qui identifie les suites de produits disponibles sur le système. Le masque de bits peut inclure les valeurs suivantes.



| Valeur retournée                                                                          | Description                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl> | Microsoft Small Business Server a été installé sur le système, mais il a peut-être été mis à niveau vers une autre version de Windows. Reportez-vous à la section Remarques pour plus d’informations sur cet indicateur de bit.<br/>                                           |
| <dl> <dt>0x00000002</dt> </dl> | Windows 10 entreprise, Windows 8.1 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition ou Windows 2000 Advanced Server est installé. Reportez-vous à la section Remarques pour plus d’informations sur cet indicateur de bit.<br/> |
| <dl> <dt>0x00000004</dt> </dl> | Les composants Microsoft BackOffice sont installés.<br/>                                                                                                                                                                                               |
| <dl> <dt>0x00000008</dt> </dl> | Communications Server 2003, Communications Server 2005, Communications Server 2007 ou Communications Server 2007 R2 sont installés.<br/>                                                                                                           |
| <dl> <dt>0x00000010</dt> </dl> | Les services Terminal Server sont installés. Cette valeur est toujours définie.<br/> Si **TerminalServer** est défini mais que **SingleUserTS** n’est pas défini, le système s’exécute en mode serveur d’applications.<br/>                                                         |
| <dl> <dt>0x00000020</dt> </dl> | Microsoft Small Business Server est installé avec la licence client restrictive en vigueur. Reportez-vous à la section Remarques pour plus d’informations sur cet indicateur de bit.<br/>                                                                            |
| <dl> <dt>0x00000040</dt> </dl> | Windows XP Embedded est installé.<br/>                                                                                                                                                                                                            |
| <dl> <dt>0x00000080</dt> </dl> | Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition ou Windows 2000 Datacenter Server est installé.<br/>                                                                                                                     |
| <dl> <dt>0x00000100</dt> </dl> | Bureau à distance est pris en charge, mais une seule session interactive est prise en charge. Cette valeur est définie, sauf si le système s’exécute en mode serveur d’applications.<br/>                                                                                       |
| <dl> <dt>0x00000200</dt> </dl> | Windows Vista Édition familiale Premium, Windows Vista Édition familiale basique ou Windows XP Édition familiale est installé.<br/>                                                                                                                                               |
| <dl> <dt>0x00000400</dt> </dl> | Windows Server 2003, Web Edition est installé.<br/>                                                                                                                                                                                               |
| <dl> <dt>0x00002000</dt> </dl> | Windows Storage Server 2003 R2 ou Windows Storage Server 2003 est installé.<br/>                                                                                                                                                                  |
| <dl> <dt>0x00004000</dt> </dl> | Windows Server 2003, Compute Cluster Edition est installé.<br/>                                                                                                                                                                                   |
| <dl> <dt>0x00008000</dt> </dl> | Windows Server famille est installé.<br/>                                                                                                                                                                                                            |



 

## <a name="remarks"></a>Notes

Vous ne devez pas compter uniquement sur l’indicateur 0x00000001 pour déterminer si Small Business Server a été installé sur le système, car cet indicateur et l’indicateur 0x00000020 sont définis lors de l’installation de cette suite de produits. Si vous mettez à niveau cette installation vers Windows Server, Standard Edition, l’indicateur 0x00000020 est désactivé, mais l’indicateur 0x00000001 reste défini. Dans ce cas, cela indique que Small Business Server a été installé sur ce système. Si cette installation est mise à niveau vers Windows Server édition entreprise, l’indicateur 0x00000001 reste défini.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Ntddk. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 




