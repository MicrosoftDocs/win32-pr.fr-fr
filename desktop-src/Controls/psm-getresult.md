---
title: Message PSM_GETRESULT (Prsht. h)
description: Utilisé par les feuilles de propriétés non modales pour récupérer les informations retournées aux feuilles de propriétés modales par feuille. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro PropSheet GetResult.
ms.assetid: e0f609ea-5d7e-4c17-ade1-3c1051c5a5bf
keywords:
- PSM_GETRESULT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PSM_GETRESULT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4acc8fed8cdaa1f4282c3ed066ad44f68221330fa9e79b0719db8bba1bca37f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169805"
---
# <a name="psm_getresult-message"></a>\_Message PSM GETRESULT

Utilisé par les feuilles de propriétés non modales pour récupérer les informations retournées aux feuilles de propriétés modales par [**feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta). Vous pouvez envoyer ce message explicitement ou utiliser la macro [**PropSheet \_ GetResult**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur positive en cas de réussite, ou-1 dans le cas contraire. Les valeurs de retour suivantes ont une signification particulière.



| Code de retour                                                                                         | Description                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ID \_ PSREBOOTSYSTEM**</dt> </dl>   | Une page a envoyé un message [**PSM \_ REBOOTSYSTEM**](psm-rebootsystem.md) à la feuille de propriétés. L’ordinateur doit être redémarré pour que les modifications apportées à l’utilisateur prennent effet.<br/> |
| <dl> <dt>**ID \_ PSRESTARTWINDOWS**</dt> </dl> | Une page a envoyé un message [**PSM \_ RESTARTWINDOWS**](psm-restartwindows.md) à la feuille de propriétés. Windows doit être redémarré pour que les modifications apportées à l’utilisateur prennent effet.<br/>  |



 

## <a name="remarks"></a>Remarques

Pour récupérer les informations d’erreur étendues, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

La valeur de retour de ce message est identique à celle que [**feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) retourne pour une feuille de propriétés modale.

[Version 5,80.](common-control-versions.md) La valeur de retour [**feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) transporte des informations différentes pour les feuilles de propriétés modales et non modales. Dans certains cas, les feuilles de propriétés non modales peuvent avoir besoin des informations qu’elles auraient reçues de **feuille** si elles avaient été modales. En particulier, il peut être nécessaire de savoir si l’ID \_ PSREBOOTSYSTEM ou l’ID \_ PSRESTARTWINDOWS aurait été retourné.

Pour une feuille de propriétés non modale, votre boucle de messages doit utiliser des [**\_ ISDIALOGMESSAGE PSM**](psm-isdialogmessage.md) pour transmettre des messages à la boîte de dialogue de la feuille de propriétés, et [**PSM \_ GETCURRENTPAGEHWND**](psm-getcurrentpagehwnd.md) pour déterminer quand détruire la boîte de dialogue. Quand l’utilisateur clique sur le bouton **OK** ou **Annuler** , **PSM \_ GETCURRENTPAGEHWND** retourne la **valeur null**. Vous pouvez ensuite récupérer la valeur qu’une feuille de propriétés modale aurait reçue de [**feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) en envoyant un message **PSM \_** .

> [!Note]  
> Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

