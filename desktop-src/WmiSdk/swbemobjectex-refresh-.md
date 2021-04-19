---
description: Met à jour les données pour les objets qui ont des données fournies par un fournisseur de performances, telles que les classes de compteur de performance. Vous pouvez obtenir des données mises à jour plus rapidement et sans appel à SWbemServices. obtenir \_ .
ms.assetid: 6aeaa336-fb98-4eda-b746-fc958198d8ae
ms.tgt_platform: multiple
title: Méthode SWbemObjectEx.Refresh_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 904e2b7f9b256596555c8396a699220108d4f37b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527803"
---
# <a name="swbemobjectexrefresh_-method"></a>SWbemObjectEx. Refresh, \_ méthode

La **méthode \_ Refresh** de [**SWbemObjectEx**](swbemobjectex.md) met à jour les données pour les objets qui ont des données fournies par un fournisseur de performances, telles que les [classes de compteur de performance](/windows/desktop/CIMWin32Prov/performance-counter-classes). Vous pouvez obtenir des données mises à jour plus rapidement et sans appel à [**SWbemServices \_ . obtenir**](swbemservices-get.md).

Pour plus d’informations sur cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
SWbemObjectEx.Refresh_( _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IFlags* \[ dans, facultatif\]
</dt> <dd>

Indicateurs d’opération réservée qui, s’ils sont spécifiés, doivent avoir la valeur 0 (zéro).

</dd> <dt>

*objWbemNamedValueSet* \[ dans, facultatif\]
</dt> <dd>

Objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui définit le contexte de l’opération.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Une fois la méthode **Refresh \_** terminée, l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Le fournisseur a échoué en interne, même si l’opération est valide.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

Le format demandé est introuvable.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Un des paramètres de l'appel n'est pas correct.

</dd> <dt>

**wbemErrRefresherBusy** -2147749975 (0x80041057)
</dt> <dd>

L'actualisateur est occupé par une autre opération.

</dd> <dt>

**wbemPartialResults** -2147745808 (0x80040010)
</dt> <dd>

Les objets, les énumérateurs ou les actualisateurs imbriqués n’ont pas tous été mis à jour. Ce retour n’est pas une erreur, mais indique que l’opération n’est pas terminée.

</dd> </dl>

## <a name="examples"></a>Exemples

L’exemple de code de script suivant montre comment obtenir des compteurs de performances bruts et cuisinés pour le processus système. Les objets sont actualisés toutes les deux secondes et les propriétés affichées.


```VB
' Get the performance counter instance for the System process
set PerfRaw = GetObject( _
    "winmgmts:win32_perfrawdata_perfproc_process.name='system'")
set PerfCooked = GetObject( _
    "winmgmts:win32_perfformatteddata_perfproc_process.name='system'")

' Display some properties in a loop
for I = 1 to 5
    Wscript.Echo "HandleCount = "& PerfRaw.HandleCount & _
         " Raw ThreadCount = " & PerfRaw.ThreadCount & _
        " Cooked ThreadCount = " & PerfCooked.ThreadCount
    
    Wscript.Sleep 2000
    
' Refresh the objects
    PerfRaw.Refresh_
    PerfCooked.Refresh_
next
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectEx<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemObjectEx<br/>                                                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SWbemObjectEx**](swbemobjectex.md)
</dt> <dt>

[Analyse des données de performances](monitoring-performance-data.md)
</dt> </dl>

 

