---
description: Les interfaces suivantes sont utilisées par une application pour gérer le package de document d’impression.
ms.assetid: 576B4527-A753-4A73-899B-896DCB8B8945
title: Imprimer les interfaces API des packages de documents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc37fa31cbda1be6927cbb24bf4b5707d10d9f2d74ed152ef630a2ad6ed588c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470121"
---
# <a name="print-document-package-api-interfaces"></a>Imprimer les interfaces API des packages de documents

Les interfaces suivantes sont utilisées par une application pour gérer le package de document d’impression.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                       | Description                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPrintDocumentPackageStatusEvent**](/windows/desktop/api/Documenttarget/nn-documenttarget-iprintdocumentpackagestatusevent)<br/>     | Représente la progression du travail d’impression.<br/>                                                                                                                                                                        |
| [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)<br/>               | Permet aux utilisateurs d’énumérer les types de cibles de package pris en charge et d’en créer un avec un ID de type donné. **IPrintDocumentPackageTarget** prend également en charge le suivi de la progression et de l’annulation de l’impression du package.<br/> |
| [**IPrintDocumentPackageTargetFactory**](/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagetargetfactory)<br/> | Utilisé avec [IPrintDocumentPackageTarget](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) pour démarrer un travail d’impression.<br/>                                                                                                               |



 

 

