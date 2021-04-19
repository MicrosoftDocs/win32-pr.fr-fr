---
description: Récupère le type et les données pour la valeur de Registre spécifiée dans une ruche de Registre hors connexion.
ms.assetid: 83604743-cb59-42a1-9951-620ad5bd8de7
title: ORGetValue, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 375dae37e2e6b6299a7bf1fd36f9b950d0433d89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541128"
---
# <a name="orgetvalue-function"></a>ORGetValue fonction)

Récupère le type et les données pour la valeur de Registre spécifiée dans une ruche de Registre hors connexion.

## <a name="syntax"></a>Syntaxe


```C++
DWORD ORGetValue(
  _In_        ORHKEY Handle,
  _In_opt_    PCWSTR lpSubKey,
  _In_opt_    PCWSTR lpValue,
  _Out_opt_   PDWORD pdwType,
  _Out_opt_   PVOID  pvData,
  _Inout_opt_ PDWORD pcbData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Gérer* \[ dans\]
</dt> <dd>

Handle d’une clé de Registre ouverte dans une ruche de Registre hors connexion.

</dd> <dt>

*lpSubKey* \[ dans, facultatif\]
</dt> <dd>

Nom de la clé de Registre. Cette clé doit être une sous-clé de la clé spécifiée par le paramètre *handle* . Ce paramètre peut être **NULL**.

Les noms de clés ne respectent pas la casse.

</dd> <dt>

*lpValue* \[ dans, facultatif\]
</dt> <dd>

Nom de la valeur de registre. Si ce paramètre a la valeur **null** ou est une chaîne vide, "", la fonction récupère le type et les données pour la valeur sans nom ou par défaut de la clé, le cas échéant. Pour plus d’informations, consultez [limites de taille des éléments du Registre](../sysinfo/registry-element-size-limits.md).

Les clés n’ont pas automatiquement une valeur sans nom ou par défaut. Les valeurs sans nom peuvent être de n’importe quel type.

Les noms de valeurs ne respectent pas la casse.

</dd> <dt>

*pdwType* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une variable qui reçoit un code indiquant le type de données stockées dans la valeur spécifiée. Pour obtenir la liste des codes de type possibles, consultez [types de valeurs de Registre](../sysinfo/registry-value-types.md). Ce paramètre peut avoir la **valeur null** si le type n’est pas requis.

</dd> <dt>

*pvData* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit les données de la valeur. Ce paramètre peut avoir la **valeur null** si les données ne sont pas requises.

Si les données sont une chaîne, la fonction recherche un caractère null de fin. Si aucun n’est trouvé, la chaîne est stockée avec une marque de fin null si la mémoire tampon est suffisamment grande pour contenir le caractère supplémentaire. Dans le cas contraire, la fonction échoue et retourne une erreur \_ plus de \_ données.

</dd> <dt>

*pcbData* \[ in, out, facultatif\]
</dt> <dd>

Pointeur vers une variable qui spécifie la taille de la mémoire tampon vers laquelle pointe le paramètre *pvData* , en octets. Quand la fonction retourne une valeur, cette variable contient la taille des données copiées dans *pvData*.

Le paramètre *pcbData* peut être **null** uniquement si *pvData* a la **valeur null**.

Si les données ont le \_ type reg SZ, \_ reg \_ multisz ou reg \_ expand \_ SZ, cette taille inclut tous les caractères null de fin. Pour plus d'informations, consultez la section Notes.

Si la mémoire tampon spécifiée par le paramètre *pvData* n’est pas assez grande pour contenir les données, la fonction retourne l’erreur \_ plus de \_ données et stocke la taille de mémoire tampon requise dans la variable vers laquelle pointe *pcbData*. Dans ce cas, le contenu de la mémoire tampon *pvData* n’est pas défini.

Si *pvData* a la **valeur null** et que *PcbData* n’a pas la **valeur null**, la fonction retourne \_ la réussite de l’erreur et stocke la taille des données, en octets, dans la variable vers laquelle pointe *pcbData*. Cela permet à une application de déterminer la meilleure façon d’allouer une mémoire tampon pour les données de la valeur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h. Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.

## <a name="remarks"></a>Notes

Une application appelle généralement la fonction [**OREnumValue**](orenumvalue.md) pour déterminer les noms de valeur, puis appelle la fonction **ORGetValue** pour récupérer les données pour les noms.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|---------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | Bibliothèque du Registre hors connexion Windows version 1,0 ou ultérieure<br/>                      |
| En-tête<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**OREnumKey**](orenumkey.md)
</dt> <dt>

[**OREnumValue**](orenumvalue.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORQueryInfoKey**](orqueryinfokey.md)
</dt> </dl>

 

 
