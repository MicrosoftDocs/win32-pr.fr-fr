---
description: L’API de script pour WMI contient des indicateurs, des valeurs communes et des codes d’erreur.
ms.assetid: feaab757-3167-420b-8f42-edced4cd4c53
ms.tgt_platform: multiple
title: Constantes d’API de script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 84e52c329fc311e7f99a6564ac51f90574308e31fa1eaa90bfb6d0bcdddc69b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130871"
---
# <a name="scripting-api-constants"></a>Constantes d’API de script

WMI utilise plusieurs types de constantes dans le paramètre *IFlags* des appels de méthode dans l' [API de script pour WMI](scripting-api-for-wmi.md).

Visual Basic applications peuvent inclure la bibliothèque de types pour l’API de script, Wbemdisp. tlb. les Scripts ne peuvent pas accéder aux constantes de la bibliothèque de types, sauf s’ils utilisent les <REFERENCE> <OBJECT> balises ou du format de fichier XML WSH (Windows script Host), comme décrit dans [utilisation de la bibliothèque de types de scripts WMI](using-the-wmi-scripting-type-library.md). Dans le cas contraire, un script doit utiliser la valeur de la constante.

## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WbemAuthenticationLevelEnum"></span><span id="wbemauthenticationlevelenum"></span><span id="WBEMAUTHENTICATIONLEVELENUM"></span>[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dd>

Définissez les niveaux d’authentification de sécurité.

</dd> <dt>

<span id="WbemChangeFlagEnum"></span><span id="wbemchangeflagenum"></span><span id="WBEMCHANGEFLAGENUM"></span>[**WbemChangeFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemchangeflagenum)
</dt> <dd>

Définir le mode d’exécution d’une opération d’écriture dans une classe ou une instance.

</dd> <dt>

<span id="WbemCimTypeEnum"></span><span id="wbemcimtypeenum"></span><span id="WBEMCIMTYPEENUM"></span>[**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)
</dt> <dd>

Définissez les types CIM valides d’une valeur de propriété.

</dd> <dt>

<span id="WbemComparisonFlagEnum"></span><span id="wbemcomparisonflagenum"></span><span id="WBEMCOMPARISONFLAGENUM"></span>[**WbemComparisonFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcomparisonflagenum)
</dt> <dd>

Définissez les paramètres pour la comparaison d’objets et sont utilisés par [**SWbemObject \_ . CompareTo**](swbemobject-compareto-.md).

</dd> <dt>

<span id="WbemConnectOptionsEnum"></span><span id="wbemconnectoptionsenum"></span><span id="WBEMCONNECTOPTIONSENUM"></span>[**WbemConnectOptionsEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemconnectoptionsenum)
</dt> <dd>

Définit un indicateur de sécurité qui est utilisé en tant que paramètre dans les appels à la méthode [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) lorsqu’une connexion à WMI sur un ordinateur distant échoue.

</dd> <dt>

<span id="WbemErrorEnum"></span><span id="wbemerrorenum"></span><span id="WBEMERRORENUM"></span>[**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)
</dt> <dd>

Définissez les erreurs qui peuvent être retournées par l' [API de script pour les appels WMI](scripting-api-for-wmi.md) .

</dd> <dt>

<span id="WbemFlagEnum"></span><span id="wbemflagenum"></span><span id="WBEMFLAGENUM"></span>[**WbemFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)
</dt> <dd>

Définit les constantes utilisées par [**SWbemServices.ExecQuery**](swbemservices-execquery.md), [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), [**SWbemServices. SubclassesOf**](swbemservices-subclassesof.md)et [**SWbemServices. InstancesOf**](swbemservices-instancesof.md).

</dd> <dt>

<span id="WbemImpersonationLevelEnum"></span><span id="wbemimpersonationlevelenum"></span><span id="WBEMIMPERSONATIONLEVELENUM"></span>[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dd>

Définissez les niveaux d’emprunt d’identité de sécurité. Ces constantes sont utilisées avec [**SWbemSecurity**](swbemsecurity.md).

</dd> <dt>

<span id="WbemObjectTextFormatEnum"></span><span id="wbemobjecttextformatenum"></span><span id="WBEMOBJECTTEXTFORMATENUM"></span>[**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)
</dt> <dd>

Définissez les formats de texte d’objet valides à utiliser par [**SWbemObjectEx \_ . GetText**](swbemobjectex-gettext-.md).

</dd> <dt>

<span id="WbemPrivilegeEnum"></span><span id="wbemprivilegeenum"></span><span id="WBEMPRIVILEGEENUM"></span>[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dd>

Définir des privilèges. Ces constantes sont utilisées avec [**SWbemSecurity**](swbemsecurity.md) pour accorder les privilèges requis pour certaines opérations.

</dd> <dt>

<span id="WbemQueryFlagEnum"></span><span id="wbemqueryflagenum"></span><span id="WBEMQUERYFLAGENUM"></span>[**WbemQueryFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemqueryflagenum)
</dt> <dd>

Définissez la profondeur de l’énumération ou de la requête, qui détermine le nombre d’objets retournés par un appel.

</dd> <dt>

<span id="WbemTextFlagEnum"></span><span id="wbemtextflagenum"></span><span id="WBEMTEXTFLAGENUM"></span>[**WbemTextFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtextflagenum)
</dt> <dd>

Définit le contenu du texte de l’objet généré et est utilisé par [**SWbemObject \_ . GetObjectText**](swbemobject-getobjecttext-.md).

</dd> <dt>

<span id="WbemTimeout"></span><span id="wbemtimeout"></span><span id="WBEMTIMEOUT"></span>[**WbemTimeout**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtimeout)
</dt> <dd>

Définit les constantes de délai d’attente. Cette constante est utilisée par [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md).

</dd> </dl>

## <a name="combining-flags"></a>Combinaison d’indicateurs

Vous pouvez combiner des indicateurs pour affecter plusieurs aspects de l’appel d’API.

Par exemple, pour créer un [*appel semi-synchrone*](gloss-s.md) , le paramètre *IFlags* dans un appel [**cQuery \_SWbemServices.Exe**](swbemservices-execquery.md) doit contenir deux indicateurs : **WbemFlagReturnImmediately** et **WbemFlagForwardOnly**. La valeur de **WbemFlagReturnImmediately** est 16 et la valeur de **WbemFlagForwardOnly** est 32. Étant donné que les constantes ne sont pas accessibles par leur nom, les valeurs de ces indicateurs sont combinées, produisant une valeur *IFlags* de 48.

L’exemple de script suivant illustre l’appel.


```VB
On Error Resume Next
For Each obj in GetObject("WinMgmts:").ExecQuery _
("SELECT * FROM Win32_NTLogEvent WHERE _ LogFile='Application'",,48)
    count  = count + 1
Next
```



Tous les indicateurs ne peuvent pas être combinés, car de nombreux sont mutuellement exclusifs et peuvent produire des résultats imprévisibles.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API de script pour WMI](scripting-api-for-wmi.md)
</dt> </dl>

 

 



