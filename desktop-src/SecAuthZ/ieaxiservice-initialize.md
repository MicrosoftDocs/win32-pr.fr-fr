---
description: vérifie et télécharge un objet ActiveX.
ms.assetid: a477c6dc-32a7-4d17-a997-6df4967d6c55
title: 'IeAxiService :: Initialize, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService.Initialize
api_type:
- COM
api_location: ''
ms.openlocfilehash: 911d955f84d81b225a1b4062e47b2b9b6ab6d058aa6df2e6a72a8d40242345a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414889"
---
# <a name="ieaxiserviceinitialize-method"></a>IeAxiService :: Initialize, méthode

la méthode **initialize** vérifie et télécharge un objet ActiveX. si l’objet satisfait aux exigences de stratégie, cette méthode initialise un objet système qui installe l’objet ActiveX.

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS Initialize(
  [in]  HWND     hwndParent,
  [in]  DWORD    dwClientPID,
  [in]  BSTR     bstrDesktop,
  [in]  BSTR     bstrClsID,
  [in]  BSTR     bstrURL,
  [out] BSTR     *pbstrNonce,
  [out] IUnknown **ppISyncBrokerInterface
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hwndParent* \[ dans\]
</dt> <dd>

handle vers la fenêtre parente de la fenêtre qui tente d’installer le contrôle de ActiveX.

</dd> <dt>

*dwClientPID* \[ dans\]
</dt> <dd>

ID de processus du processus appelant.

</dd> <dt>

*bstrDesktop* \[ dans\]
</dt> <dd>

Bureau de l’objet.

</dd> <dt>

*bstrClsID* \[ dans\]
</dt> <dd>

ID de classe de l’objet ActiveX à installer.

</dd> <dt>

*du bstrURL* \[ dans\]
</dt> <dd>

URL de l’objet ActiveX à installer.

</dd> <dt>

*pbstrNonce* \[ à\]
</dt> <dd>

contexte qui peut être utilisé pour partager des informations d’état dans les appels à d’autres méthodes utilisées pour vérifier et télécharger l’objet ActiveX.

</dd> <dt>

*ppISyncBrokerInterface* \[ à\]
</dt> <dd>

pointeur vers l’instance de l’interface [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) qui installe le contrôle ActiveX.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est S \_ OK.

Si la fonction échoue, la valeur de retour peut être l’un des codes d’erreur suivants.



| Code/valeur de retour                                                                                                                                                              | Description                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> Niveau de <dt>**confiance \_ E \_ sujet \_ non \_ approuvé**</dt> <dt>0x800B0004</dt> </dl> | l’objet ActiveX ne doit pas être installé.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows vista Business, Windows vista Enterprise, Windows les applications de bureau vista Ultimate \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiService est défini en tant que E9E92380-9ECD-4982-A0EB-6815A56CCF27<br/>                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IeAxiService**](ieaxiservice.md)
</dt> </dl>

 

 




