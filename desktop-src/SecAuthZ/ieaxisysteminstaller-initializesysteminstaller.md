---
description: Installe l’objet ActiveX spécifié.
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867813"
---
# <a name="ieaxisysteminstallerinitializesysteminstaller-method"></a>IeAxiSystemInstaller :: InitializeSystemInstaller, méthode

La méthode **InitializeSystemInstaller** installe l’objet ActiveX spécifié.

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

Pointeur vers une instance de l’interface [**IeAxiServiceCallback**](ieaxiservicecallback.md) qui vérifie si l’objet ActiveX est autorisé à être installé.

</dd> <dt>

*pbstrNonce* \[ à\]
</dt> <dd>

Contexte qui peut être utilisé pour partager des informations d’État dans les appels à d’autres méthodes utilisées pour vérifier et télécharger l’objet ActiveX.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, la méthode retourne S \_ OK.

Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](/windows/desktop/SecCrypto/common-hresult-values).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista Professionnel, Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiSystemInstaller est défini en tant que a50ea6f8-4764-4299-B309-022b2a8b4d8d<br/>                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IeAxiSystemInstaller**](ieaxisysteminstaller.md)
</dt> </dl>

 

