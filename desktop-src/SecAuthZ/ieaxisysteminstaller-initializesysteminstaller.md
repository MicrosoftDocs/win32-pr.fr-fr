---
description: installe l’objet ActiveX spécifié.
ms.assetid: c5d460d8-0df4-437a-a59e-707bf868a339
title: 'IeAxiSystemInstaller :: InitializeSystemInstaller, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller.InitializeSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: 874bee80e23051d5dfdd22e259395293ae532619
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096069"
---
# <a name="ieaxisysteminstallerinitializesysteminstaller-method"></a>IeAxiSystemInstaller :: InitializeSystemInstaller, méthode

la méthode **InitializeSystemInstaller** installe l’objet ActiveX spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT InitializeSystemInstaller(
  [in]  BSTR     bstrUrl,
  [in]  DWORD    dwClientPID,
  [in]  IUnknown *pCallback,
  [out] BSTR     *pbstrNonce
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*du bstrURL* \[ dans\]
</dt> <dd>

URL de l’objet ActiveX à installer.

</dd> <dt>

*dwClientPID* \[ dans\]
</dt> <dd>

ID de processus du processus appelant.

</dd> <dt>

*pCallback* \[ dans\]
</dt> <dd>

pointeur vers une instance de l’interface [**IeAxiServiceCallback**](ieaxiservicecallback.md) qui vérifie si l’objet ActiveX est autorisé à être installé.

</dd> <dt>

*pbstrNonce* \[ à\]
</dt> <dd>

contexte qui peut être utilisé pour partager des informations d’état dans les appels à d’autres méthodes utilisées pour vérifier et télécharger l’objet ActiveX.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la méthode est réussie, la méthode retourne S \_ OK.

Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](/windows/desktop/SecCrypto/common-hresult-values).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows vista Business, Windows vista Enterprise, Windows les applications de bureau vista Ultimate \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiSystemInstaller est défini en tant que a50ea6f8-4764-4299-B309-022b2a8b4d8d<br/>                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IeAxiSystemInstaller**](ieaxisysteminstaller.md)
</dt> </dl>

 

