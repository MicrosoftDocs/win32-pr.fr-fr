---
description: Spécifie ce que le spouleur effectue actuellement lors du traitement d’un travail d’impression XPS.
ms.assetid: 4fa5b749-e4f9-4f08-97b5-e58f82d0b485
title: EPrintXPSJobProgress, énumération (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EPrintXPSJobProgress
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ef3d72d983388c022afbb0e914f87a17587f70b8e175dd57dabcd61d224e93bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949639"
---
# <a name="eprintxpsjobprogress-enumeration"></a>Énumération EPrintXPSJobProgress

Spécifie ce que le spouleur effectue actuellement lors du traitement d’un travail d’impression XPS.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagEPrintXPSJobProgress { 
  kAddingDocumentSequence,
  kDocumentSequenceAdded,
  kAddingFixedDocument,
  kFixedDocumentAdded,
  kAddingFixedPage,
  kFixedPageAdded,
  kResourceAdded,
  kFontAdded,
  kImageAdded,
  kXpsDocumentCommitted
} EPrintXPSJobProgress;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="kAddingDocumentSequence"></span><span id="kaddingdocumentsequence"></span><span id="KADDINGDOCUMENTSEQUENCE"></span>**kAddingDocumentSequence**
</dt> <dd>

Une séquence de documents va être ajoutée à la tâche XPS.

</dd> <dt>

<span id="kDocumentSequenceAdded"></span><span id="kdocumentsequenceadded"></span><span id="KDOCUMENTSEQUENCEADDED"></span>**kDocumentSequenceAdded**
</dt> <dd>

Une séquence de documents a été ajoutée à la tâche XPS.

</dd> <dt>

<span id="kAddingFixedDocument"></span><span id="kaddingfixeddocument"></span><span id="KADDINGFIXEDDOCUMENT"></span>**kAddingFixedDocument**
</dt> <dd>

Un document fixe va être ajouté à la tâche XPS.

</dd> <dt>

<span id="kFixedDocumentAdded"></span><span id="kfixeddocumentadded"></span><span id="KFIXEDDOCUMENTADDED"></span>**kFixedDocumentAdded**
</dt> <dd>

Un document fixe a été ajouté à la tâche XPS.

</dd> <dt>

<span id="kAddingFixedPage"></span><span id="kaddingfixedpage"></span><span id="KADDINGFIXEDPAGE"></span>**kAddingFixedPage**
</dt> <dd>

Une page va être ajoutée au travail XPS.

</dd> <dt>

<span id="kFixedPageAdded"></span><span id="kfixedpageadded"></span><span id="KFIXEDPAGEADDED"></span>**kFixedPageAdded**
</dt> <dd>

Une page a été ajoutée à la tâche XPS.

</dd> <dt>

<span id="kResourceAdded"></span><span id="kresourceadded"></span><span id="KRESOURCEADDED"></span>**kResourceAdded**
</dt> <dd>

Une ressource a été ajoutée à la tâche XPS.

</dd> <dt>

<span id="kFontAdded"></span><span id="kfontadded"></span><span id="KFONTADDED"></span>**kFontAdded**
</dt> <dd>

Une police a été ajoutée à la tâche XPS.

</dd> <dt>

<span id="kImageAdded"></span><span id="kimageadded"></span><span id="KIMAGEADDED"></span>**kImageAdded**
</dt> <dd>

Une image a été ajoutée à la tâche XPS.

</dd> <dt>

<span id="kXpsDocumentCommitted"></span><span id="kxpsdocumentcommitted"></span><span id="KXPSDOCUMENTCOMMITTED"></span>**kXpsDocumentCommitted**
</dt> <dd>

Les données de la tâche XPS ont été validées.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette énumération est principalement utilisée comme paramètre pour la fonction [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) .

Ces valeurs peuvent faire référence à la phase de mise en file d’attente ou de rendu d’un travail d’impression.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |



 

 




