---
title: Méthode WSMan. CreateResourceLocator (WSManDisp. h)
description: Crée un objet ResourceLocator qui peut être utilisé au lieu de spécifier un URI de ressource dans les opérations d’objet de session, telles que session. obtenir, session. put ou session. Enumerate.
ms.assetid: 1b04fe11-ec90-4374-9838-a0df313b722e
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode CreateResourceLocator
- Méthode CreateResourceLocator Windows Remote Management, objet WSMan
- Objet WSMan Windows Remote Management, méthode CreateResourceLocator
topic_type:
- apiref
api_name:
- WSMan.CreateResourceLocator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6982d1ea0b257ca9276918931ce233e675fd3eb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942041"
---
# <a name="wsmancreateresourcelocator-method"></a>Méthode WSMan. CreateResourceLocator

Crée un objet [**ResourceLocator**](resourcelocator.md) qui peut être utilisé au lieu de spécifier un URI de ressource dans les opérations d’objet de [**session**](session.md) , telles que [**session. obtenir**](session-get.md), [**session. put**](session-put.md)ou [**session. Enumerate**](session-enumerate.md).

## <a name="syntax"></a>Syntaxe


```VB
WSMan.CreateResourceLocator( _
  [ ByVal uri ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*URI* \[ dans, facultatif\]
</dt> <dd>

URI de ressource pour la ressource. Pour plus d’informations sur les chaînes d’URI, consultez [URI de ressource](resource-uris.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Objet [**ResourceLocator**](resourcelocator.md) qui peut ensuite être utilisé pour effectuer des opérations WinRM locales ou distantes.

## <a name="remarks"></a>Notes

Si la propriété **FragmentDialect** n’est pas spécifiée dans l’objet [**ResourceLocator**](resourcelocator.md) , la valeur par défaut est la spécification XPath 1,0. Pour plus d’informations, consultez [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant crée un objet [**ResourceLocator**](resourcelocator.md) et obtient la valeur de la propriété **Description** de la carte réseau à partir de l’instance de [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) avec un index de « 1 ».


```VB
const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
const FragmentPath = "Description"

Set objWSMan = CreateObject("WSMan.Automation")

Set objSession = objWSMan.CreateSession()

Set objLocator = objWSMan.CreateResourceLocator(Uri)

objLocator.AddSelector "Index", "1"
objLocator.FragmentPath = FragmentPath

Dim Xml
Xml = objSession.Get(objLocator)
WScript.Echo Xml
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> <dt>

[**session**](session.md)
</dt> </dl>

 

