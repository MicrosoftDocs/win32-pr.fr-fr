---
description: La \_ méthode CompareTo de l’objet SWbemLastError compare deux objets SWbemObject. Cette comparaison est soumise à certaines contraintes basées sur les valeurs spécifiées dans le paramètre iFlags.
ms.assetid: 541510e4-ef8d-4436-966f-19c5df422281
ms.tgt_platform: multiple
title: Méthode SWbemLastError.CompareTo_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.CompareTo_
- ISWbemLastError.CompareTo_
- ISWbemLastError.CompareTo_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cc169b8a18f97cd6fd8f51a0e8d1456e3619cfbebf0cbf1f107adfac2787bb54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314593"
---
# <a name="swbemlasterrorcompareto_-method"></a>SWbemLastError. CompareTo, \_ méthode

La **méthode \_ CompareTo** de l’objet [**SWbemLastError**](swbemlasterror.md) compare deux objets [**SWbemObject**](swbemobject.md) . Cette comparaison est soumise à certaines contraintes basées sur les valeurs spécifiées dans le paramètre *IFlags* .

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
bAreEqual = .CompareTo_( _
  ByVal objwbemObject, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*objwbemObject* \[ dans\]
</dt> <dd>

Obligatoire. Objet de classe [**SWbemObject**](swbemobject.md) . Ce paramètre est l’objet avec lequel le premier objet est comparé. L’objet doit être une instance **SWbemObject** valide.

</dd> <dt>

*IFlags* \[ dans, facultatif\]
</dt> <dd>

Entier qui spécifie des indicateurs supplémentaires pour l’opération. Ce paramètre spécifie les caractéristiques d’objet à prendre en compte lorsque les comparaisons d’objets sont effectuées. Vous pouvez utiliser **wbemComparisonFlagIncludeAll** pour prendre en compte toutes les fonctionnalités (par défaut) ou n’importe quelle combinaison des valeurs suivantes.

<dt>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>wbemComparisonFlagIncludeAll * * * * (0 (0x0))


</dt> <dd>

Fait en sorte que toutes les propriétés, qualificateurs et versions soient comparés.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>wbemComparisonFlagIgnoreQualifiers * * * * (1 (0x1))


</dt> <dd>

Fait en sorte que tous les qualificateurs (y compris la **clé** et le **dynamique**) soient ignorés en comparaison.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>wbemComparisonFlagIgnoreObjectSource * * * * (2 (0X2))


</dt> <dd>

Fait en sorte que la source des objets, à savoir le serveur et l’espace de noms dont ils proviennent, soit ignorée par rapport aux autres objets.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>wbemComparisonFlagIgnoreDefaultValues * * * * (4 (0x4))


</dt> <dd>

Entraîne l’ignorance des valeurs par défaut des propriétés. Cet indicateur est significatif uniquement lors de la comparaison de classes.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>wbemComparisonFlagIgnoreClass * * * * (8 (0x8))


</dt> <dd>

Indique au système de supposer que les objets comparés sont des instances de la même classe. Par conséquent, cet indicateur ne compare que les informations relatives à l’instance. Utilisez cet indicateur pour optimiser les performances. Si les objets ne sont pas de la même classe, les résultats sont non définis.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>wbemComparisonFlagIgnoreCase * * * * (16 (0x10))


</dt> <dd>

Fait en sorte que les valeurs de chaîne soient comparées sans respect de la casse. Cela s’applique à la fois aux chaînes et aux valeurs de qualificateur. Les noms de propriétés et de qualificateurs sont toujours comparés sans distinction minuscules/majuscules, que cet indicateur soit spécifié ou non.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>wbemComparisonFlagIgnoreFlavor * * * * (32 (0x20))


</dt> <dd>

Fait en sorte que les versions de qualificateur soient ignorées. Cet indicateur tient compte des valeurs de qualificateur, mais ignore les distinctions de version telles que les règles de propagation et les restrictions de substitution.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

La **méthode \_ CompareTo** retourne la valeur booléenne **true** si les objets correspondent ; sinon, elle retourne **false**.

## <a name="error-codes"></a>Codes d’erreur

À la fin de la **méthode \_ CompareTo** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erreur non spécifiée.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Un paramètre spécifié n’est pas valide.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Mémoire insuffisante pour terminer l’opération.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLastError<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemLastError<br/>                                                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SWbemLastError**](swbemlasterror.md)
</dt> <dt>

[**M**](swbemobject.md)
</dt> </dl>

 

 




