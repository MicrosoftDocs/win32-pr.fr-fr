---
title: Session. Enumerate, méthode (WSManDisp. h)
description: Énumère une table, une collection de données ou une ressource de journal.
ms.assetid: ed8ad3ad-d033-45cb-b681-995c5f73b12e
ms.tgt_platform: multiple
keywords:
- énumération de la méthode Windows Remote Management
- énumérer la méthode Windows Remote Management, objet Session
- Windows Remote Management d’objet de Session, énumération, méthode
topic_type:
- apiref
api_name:
- Session.Enumerate
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dc40a45cc28179acd8e5dc9fff17df8b8accddd8dffda3ea299571e11d46564
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642629"
---
# <a name="sessionenumerate-method"></a>Session. Enumerate, méthode

Énumère une table, une collection de données ou une ressource de journal. Pour créer une requête, incluez un paramètre de *filtre* et un paramètre de *dialecte* dans une énumération. Vous pouvez également utiliser un objet [**ResourceLocator**](resourcelocator.md) pour créer des requêtes. Pour plus d’informations, consultez [énumération ou liste de toutes les instances d’une ressource](enumerating-or-listing-all-instances-of-a-resource.md).

## <a name="syntax"></a>Syntaxe


```VB
Session.Enumerate( _
  ByVal resourceUri, _
  [ ByVal filter ], _
  [ ByVal dialect ], _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*resourceuri* \[ dans\]
</dt> <dd>

Identificateur de la ressource à récupérer.

Ce paramètre peut contenir l’un des éléments suivants :

-   URI de la ressource.

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service"
    ```

    

-   Objet [**ResourceLocator**](resourcelocator.md) .
-   Une référence de point de terminaison [*WS-Addressing*](windows-remote-management-glossary.md) , comme décrit dans la norme de protocole WS-Management. Pour plus d’informations sur la spécification publique pour [protocole WS-Management](ws-management-protocol.md), consultez la [page index des spécifications de gestion](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*filtre* \[ dans, facultatif\]
</dt> <dd>

Filtre qui définit les éléments de la ressource qui sont retournés par l’énumération. Lorsque la ressource est énumérée, seuls les éléments qui correspondent aux critères de filtre sont retournés. L’inclusion d’un paramètre de *filtre* et d’un paramètre de *dialecte* dans une énumération convertit l’énumération en requête. Pour obtenir un exemple, consultez [interrogation d’instances spécifiques d’une ressource](querying-for-specific-instances-of-a-resource.md).

Si vous avez un objet [**ResourceLocator**](resourcelocator.md) pour le paramètre *resourceURI* , ce paramètre ne doit pas être utilisé.

</dd> <dt>

*dialecte* \[ dans, facultatif\]
</dt> <dd>

Langue utilisée par le filtre. [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi), un sous-ensemble de SQL utilisé par WMI, est le seul langage pris en charge.

Si vous avez un objet [**ResourceLocator**](resourcelocator.md) pour le paramètre *resourceURI* , ce paramètre ne doit pas être utilisé.

</dd> <dt>

*indicateurs* \[ dans, facultatif\]
</dt> <dd>

Paramètre qui doit contenir un indicateur dans l’énumération **\_ \_ WSManEnumFlags** . Pour plus d’informations, consultez [énumération, constantes](enumeration-constants.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Objet [**énumérateur**](enumerator.md) qui contient les résultats de l’énumération.

## <a name="remarks"></a>Remarques

Pour plus d’informations sur la limitation des appels réseau pendant une énumération, consultez la propriété [**BatchItems**](session-batchitems.md) .

sachez que si les indicateurs incluent les [**constantes d’énumération**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** ou **WSManFlagHierarchyShallow** , Windows Remote Management service retourne le code d’erreur le **MODE de \_ polymorphisme WSMAN n’est pas \_ \_ \_ pris en charge**.

Si un filtre est spécifié, il doit s’agir d’un document valide en ce qui concerne le schéma de la ressource. Le paramètre de dialecte est facultatif. Toutefois, si la chaîne de filtre commence par <, mais n’est pas un fragment XML, vous devez inclure le paramètre de *dialecte* ou définir l’indicateur **WSManFlagNonXmlText** dans le paramètre *Flags* . Pour plus d’informations, consultez [**énumération, constantes**](enumeration-constants.md).

La méthode C++ correspondante est [**IWSManSession :: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant énumère les instances de [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) sur un ordinateur distant spécifié par le nom de domaine complet (ServerName.domain.com). N’oubliez pas que la libération de l’objet d’énumération efface les demandes d’énumération en attente. La sous-routine DisplayOutput utilise le fichier de transformation XML de l’outil en ligne de commande WinRM (WsmTxt. Xsl) pour générer les données sous forme de tableau.


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject( "WSMan.Automation" )

Set objSession = objWsman.CreateSession( "https://" & REMOTECOMPUTER )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_LogicalDisk"

Set objResultSet = objSession.Enumerate( strResource )

While Not objResultSet.AtEndOfStream
 
 DisplayOutput( objResultSet.ReadItem ) 

Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile ) 
End Sub
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

[**Session**](session.md)
</dt> <dt>

[Interrogation d’instances spécifiques d’une ressource](querying-for-specific-instances-of-a-resource.md)
</dt> <dt>

[**BatchItems**](session-batchitems.md)
</dt> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

