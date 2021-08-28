---
description: Gère les messages d’État et d’erreur pendant les transferts de données d’image et les affiche à l’utilisateur.
ms.assetid: 23e85c63-80b9-4510-854d-289c8d23be2d
title: 'IWiaErrorHandler :: ReportStatus, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler.ReportStatus
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 6604dc8dbf0cad5f31449ff3cc30945c1e6059727d513fa98dbf436eb199f70f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659749"
---
# <a name="iwiaerrorhandlerreportstatus-method"></a>IWiaErrorHandler :: ReportStatus, méthode

Gère les messages d’État et d’erreur pendant les transferts de données d’image et les affiche à l’utilisateur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ReportStatus(
  [in] HWND     hwndParent,
  [in] IUnknown *punkItem,
  [in] HRESULT  hrStatus,
  [in] LONG     cbResLength,
  [in] BYTE     *pbData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hwndParent* \[ dans\]
</dt> <dd>

Type : **HWND**

**HWND** qui est la fenêtre parente pour la fenêtre de message.

</dd> <dt>

*punkItem* \[ dans\]
</dt> <dd>

Type : **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Pointeur vers l’interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) de l’élément en cours de transfert. Cet objet implémente au minimum [**IWiaItem2**](-wia-iwiaitem2.md) et [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).

</dd> <dt>

*hrStatus* \[ dans\]
</dt> <dd>

Type : **HRESULT**

**HRESULT** qui correspond au code d’état reçu par [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).

</dd> <dt>

*cbResLength* \[ dans\]
</dt> <dd>

Type : **long**

**Valeur de type long** qui correspond à la taille des données référencées par *pbData*.

</dd> <dt>

*pbData* \[ dans\]
</dt> <dd>

Type : **Byte \***

Pointeur vers la mémoire tampon de données telle qu’elle a été reçue par [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Retourne *hrStatus* si l’erreur ne peut pas être récupérée à partir de. Dans le cas contraire, elle retourne l’une des valeurs suivantes.



| Code de retour                                                                             | Description                                                                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>    | L’action appropriée a été prise pour corriger l’erreur et le transfert peut se poursuivre. <br/> |
| <dl> <dt>**S \_ false**</dt> </dl> | Aucune action n’a été prise pour gérer l’état d’erreur ou de rapport à l’utilisateur. <br/>                |
| <dl> <dt>**E \_ Abort**</dt> </dl> | L’utilisateur a choisi d’abandonner le transfert en réponse à la boîte de dialogue affichée. <br/>        |



 

## <a name="remarks"></a>Remarques

Windows L’acquisition d’images (WIA) 2,0 appelle **IWiaErrorHandler :: ReportStatus** lorsque le pilote envoie un message d’état de l' **\_ \_ appareil \_ MSG MSG** à [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback). Cette méthode gère le message et affiche des informations à l’utilisateur sur l’État ou l’erreur. Si le message concerne une erreur, la méthode permet à l’utilisateur de choisir, si possible, s’il faut essayer de récupérer à partir de l’erreur et continuer le transfert ou l’abandonner.

*hrStatus* est défini sur WIA \_ Status \_ Transfer \_ Begin pour informer le gestionnaire qu’un transfert a démarré. Elle est définie sur \_ \_ la fin du transfert d’État WIA une \_ fois le transfert terminé.

Si le niveau de gravité de la valeur de *hrStatus* est \_ réussite, l’utilisateur doit être autorisé à annuler le transfert.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
