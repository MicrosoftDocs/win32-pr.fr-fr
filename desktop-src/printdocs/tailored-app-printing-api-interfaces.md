---
description: Les interfaces suivantes sont utilisées par une application pour gérer le package de document d’impression.
ms.assetid: 576B4527-A753-4A73-899B-896DCB8B8945
title: Imprimer les interfaces API des packages de documents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adc495be5c58598d00250568ff852cf4f897e0b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235566"
---
# <a name="print-document-package-api-interfaces"></a>Imprimer les interfaces API des packages de documents

Les interfaces suivantes sont utilisées par une application pour gérer le package de document d’impression.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                       | Description                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPrintDocumentPackageStatusEvent**](/windows/desktop/api/Documenttarget/nn-documenttarget-iprintdocumentpackagestatusevent)<br/>     | Représente la progression du travail d’impression.<br/>                                                                                                                                                                        |
| [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)<br/>               | Permet aux utilisateurs d’énumérer les types de cibles de package pris en charge et d’en créer un avec un ID de type donné. **IPrintDocumentPackageTarget** prend également en charge le suivi de la progression et de l’annulation de l’impression du package.<br/> |
| [**IPrintDocumentPackageTargetFactory**](/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagetargetfactory)<br/> | Utilisé avec [IPrintDocumentPackageTarget](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) pour démarrer un travail d’impression.<br/>                                                                                                               |



 

 

