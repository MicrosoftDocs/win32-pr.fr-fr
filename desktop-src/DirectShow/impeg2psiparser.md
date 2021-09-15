---
description: l’implémentation de cette interface est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow.
ms.assetid: a18fc6b6-f37e-4c87-9150-0504333d33c2
title: Interface IMpeg2PsiParser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser
api_type:
- COM
api_location: ''
ms.openlocfilehash: 51f0f3373c67da75c50ecc2f6bc234e0351f5dc3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413981"
---
# <a name="impeg2psiparser-interface"></a>Interface IMpeg2PsiParser

l’implémentation de cette interface est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow. il ne s’agit pas d’une API DirectShow prise en charge.

l' `IMpeg2PsiParser` interface récupère les informations spécifiques au programme (psi) à partir du filtre de l’analyseur psi, fourni dans le kit de développement logiciel (SDK) DirectShow sous la forme d’un exemple de filtre. Une application peut utiliser ce filtre pour mapper les ID de programme (PID) sur le filtre de démultiplexage MPEG-2.

## <a name="members"></a>Membres

L’interface **IMpeg2PsiParser** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IMpeg2PsiParser** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IMpeg2PsiParser** possède ces méthodes.



| Méthode                                                                             | Description                                                                               |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**FindRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd407137(v=vs.85))         | Recherche le PID d’un programme, en fonction du numéro de programme.<br/> |
| [**GetCountOfElementaryStreams**](impeg2psiparser-getcountofelementarystreams.md) | Récupère le nombre de flux élémentaires dans un programme spécifié.<br/>             |
| [**GetCountOfPrograms**](impeg2psiparser-getcountofprograms.md)                   | Récupère le nombre de programmes dans le flux de transport.<br/>                      |
| [**GetPatVersionNumber**](impeg2psiparser-getpatversionnumber.md)                 | Récupère le champ du \_ numéro de version de la table d’association de programmes (Pat).<br/>  |
| [**GetPmtVersionNumber**](impeg2psiparser-getpmtversionnumber.md)                 | Récupère le champ du \_ numéro de version à partir d’un PMT spécifié.<br/>                      |
| [**GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85))           | Récupère l’attribution de PID pour un flux élémentaire spécifié dans un programme.<br/>   |
| [**GetRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd376624(v=vs.85))           | Récupère l’attribution de PID pour un PMT spécifié.<br/>                              |
| [**GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md)           | Récupère le numéro de programme d’un programme spécifié.<br/>                          |
| [**GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85))                 | Récupère le type de flux pour un flux élémentaire spécifié dans un programme.<br/>      |
| [**GetTransportStreamId**](impeg2psiparser-gettransportstreamid.md)               | Récupère le \_ \_ champ d’ID de flux de transport à partir de Pat.<br/>                        |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Exemple de filtre de l’analyseur PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 
