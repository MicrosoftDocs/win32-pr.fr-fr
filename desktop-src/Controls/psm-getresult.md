---
title: Message PSM_GETRESULT (Prsht. h)
description: Utilisé par les feuilles de propriétés non modales pour récupérer les informations retournées aux feuilles de propriétés modales par feuille. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro PropSheet GetResult.
ms.assetid: e0f609ea-5d7e-4c17-ade1-3c1051c5a5bf
keywords:
- PSM_GETRESULT les contrôles de message Windows
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
ms.openlocfilehash: d41609f625cbd3938fa78e9a2f91ab70168ecc29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509077"
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
| <dl> <dt>**ID \_ PSRESTARTWINDOWS**</dt> </dl> | Une page a envoyé un message [**PSM \_ RESTARTWINDOWS**](psm-restartwindows.md) à la feuille de propriétés. Vous devez redémarrer Windows pour que les modifications apportées à l’utilisateur prennent effet.<br/>  |



 

## <a name="remarks"></a>Notes

Pour récupérer les informations d’erreur étendues, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

La valeur de retour de ce message est identique à celle que [**feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) retourne pour une feuille de propriétés modale.

[Version 5,80.](common-control-versions.md) La valeur de retour [**feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) transporte des informations différentes pour les feuilles de propriétés modales et non modales. Dans certains cas, les feuilles de propriétés non modales peuvent avoir besoin des informations qu’elles auraient reçues de **feuille** si elles avaient été modales. En particulier, il peut être nécessaire de savoir si l’ID \_ PSREBOOTSYSTEM ou l’ID \_ PSRESTARTWINDOWS aurait été retourné.

Pour une feuille de propriétés non modale, votre boucle de messages doit utiliser des [**\_ ISDIALOGMESSAGE PSM**](psm-isdialogmessage.md) pour transmettre des messages à la boîte de dialogue de la feuille de propriétés, et [**PSM \_ GETCURRENTPAGEHWND**](psm-getcurrentpagehwnd.md) pour déterminer quand détruire la boîte de dialogue. Quand l’utilisateur clique sur le bouton **OK** ou **Annuler** , **PSM \_ GETCURRENTPAGEHWND** retourne la **valeur null**. Vous pouvez ensuite récupérer la valeur qu’une feuille de propriétés modale aurait reçue de [**feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) en envoyant un message **PSM \_** .

> [!Note]  
> Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

