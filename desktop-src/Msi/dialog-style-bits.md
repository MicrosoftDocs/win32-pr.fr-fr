---
description: Le style d’une boîte de dialogue est spécifié dans la colonne attributs de la table de boîte de dialogue par un mot de 32 bits composé d’indicateurs de bits de style.
ms.assetid: aad719e8-86b3-4b2b-b417-db55013f8d3a
title: Bits de style de boîte de dialogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43742c61c8dfe0827d0d51c7f9c8a2de60116500b6fdca3e404a08e120ac4348
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947441"
---
# <a name="dialog-style-bits"></a>Bits de style de boîte de dialogue

Le style d’une boîte de dialogue est spécifié dans la colonne attributs de la [table de boîte de dialogue](dialog-table.md) par un mot de 32 bits composé d’indicateurs de bits de style.

La liste suivante fournit des liens vers les descriptions des bits de style boîte de dialogue réservés.



| Nom                                                      | Decimal | Valeur hexadécimale | Constante                                                                                                                                       |
|-----------------------------------------------------------|---------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [Visible](visible-dialog-style-bit.md)                   | 1       | 0x00000001  | **msidbDialogAttributesVisible**                                                                                                               |
| [Modal](modal-dialog-style-bit.md)                       | 2       | 0x00000002  | **msidbDialogAttributesModal**                                                                                                                 |
| [Réduire](minimize-dialog-style-bit.md)                 | 4       | 0x00000004  | **msidbDialogAttributesMinimize**                                                                                                              |
| [SysModal](sysmodal-dialog-style-bit.md)                 | 8       | 0x00000008  | **msidbDialogAttributesSysModal**                                                                                                              |
| [KeepModeless](keepmodeless-dialog-style-bit.md)         | 16      | 0x00000010  | **msidbDialogAttributesKeepModeless**                                                                                                          |
| [TrackDiskSpace](trackdiskspace-dialog-style-bit.md)     | 32      | 0x00000020  | **msidbDialogAttributesTrackDiskSpace**                                                                                                        |
| [UseCustomPalette](usecustompalette-dialog-style-bit.md) | 64      | 0x00000040  | **msidbDialogAttributesUseCustomPalette**                                                                                                      |
| [RTLRO](rtlro-dialog-style-bit.md)                       | 128     | 0x00000080  | **msidbDialogAttributesRTLRO**                                                                                                                 |
| [RightAligned](rightaligned-dialog-style-bit.md)         | 256     | 0x00000100  | **msidbDialogAttributesRightAligned**                                                                                                          |
| [LeftScroll](leftscroll-dialog-style-bit.md)             | 512     | 0x00000200  | **msidbDialogAttributesLeftScroll**                                                                                                            |
| [BiDi](bidi-dialog-style-bit.md)                         | 896     | 0x00000380  | **msidbDialogAttributesBiDi**  =  **msidbDialogAttributesRTLRO** \| **msidbDialogAttributesRightAligned** \| **msidbDialogAttributesLeftScroll** |
| [Error](error-dialog-style-bit.md)                       | 65536   | 0x00010000  | **msidbDialogAttributesError**                                                                                                                 |



 

 

 



