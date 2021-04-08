---
title: Méthodes de propriété IADsSession (IADs. h)
description: Les méthodes de propriété de l’interface IADsSession obtiennent ou définissent les propriétés décrites dans le tableau suivant. Pour plus d’informations et pour obtenir une discussion générale sur les méthodes de propriété, consultez Méthodes de propriété d’interface.
ms.assetid: b2366da7-c51c-4279-8931-2000d3110d72
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsSession ADSI
topic_type:
- apiref
api_name:
- IADsSession Property Methods
- IADsSession.Computer
- IADsSession.get_Computer
- IADsSession.ComputerPath
- IADsSession.get_ComputerPath
- IADsSession.ConnectTime
- IADsSession.get_ConnectTime
- IADsSession.IdleTime
- IADsSession.get_IdleTime
- IADsSession.User
- IADsSession.get_User
- IADsSession.UserPath
- IADsSession.get_UserPath
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cf7dd9abe25d731ba63385cd8d632c4212ea349
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843441"
---
# <a name="iadssession-property-methods"></a>Méthodes de propriété IADsSession

Les méthodes de propriété de l’interface [**IADsSession**](/windows/desktop/api/Iads/nn-iads-iadssession) obtiennent ou définissent les propriétés décrites dans le tableau suivant. Pour plus d’informations et pour obtenir une discussion générale sur les méthodes de propriété, consultez [méthodes de propriété d’interface](interface-property-methods.md).

## <a name="properties"></a>Propriétés

<dl> <dt>

**Ordinateur**
</dt> <dd> <dl>

Nom de la station de travail cliente.

<dt>

Type d'accès : Lecture seule
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Computer(
  [out] BSTR* pbstrComputer
);
```


</dt> </dl> </dd> <dt>

**ComputerPath**
</dt> <dd> <dl>

ADsPath de l’objet ordinateur pour la station de travail cliente.

<dt>

Type d'accès : Lecture seule
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerPath(
  [out] BSTR* pbstrComputerPath
);
```


</dt> </dl> </dd> <dt>

**ConnectTime**
</dt> <dd> <dl>

Temps écoulé, en secondes, depuis le début de la session.

<dt>

Type d'accès : Lecture seule
</dt> <dt>

Type de données de script : **long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ConnectTime(
  [out] LONG* plConnectTime
);
```


</dt> </dl> </dd> <dt>

**IdleTime**
</dt> <dd> <dl>

Durée d’inactivité, en secondes, de la session.

<dt>

Type d'accès : Lecture seule
</dt> <dt>

Type de données de script : **long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IdleTime(
  [out] LONG* plIdleTime
);
```


</dt> </dl> </dd> <dt>

**Utilisateur**
</dt> <dd> <dl>

Nom de l’utilisateur de la session.

<dt>

Type d'accès : Lecture seule
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_User(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> <dt>

**UserPath**
</dt> <dd> <dl>

ADsPath de l’objet utilisateur pour l’utilisateur de cette session.

<dt>

Type d'accès : Lecture seule
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserPath(
  [out] BSTR* pbstrUserPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Exemples

L’exemple de code suivant montre comment examiner des sessions pour un service de fichiers.


```VB
Dim fso As IADsFileServiceOperations
On Error GoTo Cleanup

' Bind to a file service operations object on "myComputer" in the local domain.
Set fso = GetObject("WinNT://myComputer/LanmanServer")

' Enumerate sessions.
If (IsEmpty(fso) = False) Then
    For Each session In fso.sessions
        MsgBox "Session Computer: " & session.Computer
        MsgBox "Session User: " & session.User
    Next Session
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fso = Nothing
```



L’exemple de code suivant énumère une collection de sessions.


```C++
IADsFileServiceOperations *pFso = NULL;
IADsSession *pSes = NULL;
IADsCollection *pColl = NULL;
HRESULT hr = S_OK;
IUnknown *pUnk = NULL;
BSTR bstr = NULL;
VARIANT var;
ULONG lFetch = 0;
IDispatch *pDisp = NULL;
IEnumVARIANT *pEnum = NULL;

VariantInit(&var);

LPWSTR adsPath = L"WinNT://aMachine/LanmanServer";

hr = ADsGetObject(adsPath,IID_IADsFileServiceOperations,
                  (void**)&pFso);

if(FAILED(hr)) {goto Cleanup;}

hr = pFso->Sessions(&pColl);

// Enumerate sessions. 
hr = pColl->get__NewEnum(&pUnk);
if(FAILED(hr)) {goto Cleanup;}

hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
if(FAILED(hr)) {goto Cleanup;}

// Enumerate.
hr = pEnum->Next(1, &var, &lFetch);
while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADsSession, (void**)&pSes);
        pSes->get_Computer(&bstr);
        printf("Session host: %S\n",bstr);
        SysFreeString(bstr);

        pSes->get_User(&bstr);
        printf("Session user: %S\n",bstr);
        SysFreeString(bstr);

        pRes->Release();
    }

    VariantClear(&var);
    pDisp=NULL;
    hr = pEnum->Next(1, &var, &lFetch);
};

Cleanup:
    if(pFso) pFso->Release();
    if(pColl) pColl->Release();
    if(pUnk) pUnk->Release();
    if(pEnum) pEnum->Release();
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsSession est défini en tant que 398B7DA0-4AAB-11CF-AE2C-00AA006EBFB9<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IADsFileServiceOperations :: sessions**](/windows/desktop/api/Iads/nf-iads-iadsfileserviceoperations-sessions)
</dt> <dt>

[**IADsSession**](/windows/desktop/api/Iads/nn-iads-iadssession)
</dt> </dl>

 

 





