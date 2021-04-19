---
description: Énumère les valeurs de la clé de Registre ouverte spécifiée dans une ruche de Registre hors connexion. La fonction récupère des informations pour une valeur sous la clé spécifiée chaque fois que la fonction est appelée.
ms.assetid: 592a404f-a35d-4d89-ad1e-d572787bcb12
title: OREnumValue, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OREnumValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b8049a5d16a88dc87bf4c0f6f5e8ef18b30beadc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524028"
---
# <a name="orenumvalue-function"></a>OREnumValue fonction)

Énumère les valeurs de la clé de Registre ouverte spécifiée dans une ruche de Registre hors connexion. La fonction récupère des informations pour une valeur sous la clé spécifiée chaque fois que la fonction est appelée.

## <a name="syntax"></a>Syntaxe


```C++
DWORD OREnumValue(
  _In_        ORHKEY Handle,
  _In_        DWORD  dwIndex,
  _Out_       PWSTR  lpValueName,
  _Inout_     PDWORD lpcValueName,
  _Out_opt_   PDWORD lpType,
  _Out_opt_   PBYTE  lpData,
  _Inout_opt_ PDWORD lpcbData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Gérer* \[ dans\]
</dt> <dd>

Handle d’une clé de Registre ouverte dans une ruche de Registre hors connexion.

</dd> <dt>

*dwIndex* \[ dans\]
</dt> <dd>

Index de la valeur à récupérer. Ce paramètre doit être égal à zéro pour le premier appel à la fonction, puis être incrémenté pour les appels suivants.

Étant donné que les valeurs ne sont pas triées, toute nouvelle valeur aura un index arbitraire. Cela signifie que la fonction peut retourner des valeurs dans n’importe quel ordre.

</dd> <dt>

*lpValueName* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit le nom de la valeur sous la forme d’une chaîne terminée par le caractère null. Cette mémoire tampon doit être suffisamment grande pour inclure le caractère null de fin.

Pour plus d’informations, consultez [limites de taille des éléments du Registre](../sysinfo/registry-element-size-limits.md).

</dd> <dt>

*lpcValueName* \[ in, out\]
</dt> <dd>

Pointeur vers une variable qui spécifie la taille de la mémoire tampon vers laquelle pointe le paramètre *lpValueName* , en caractères. Quand la fonction retourne, la variable reçoit le nombre de caractères stockés dans la mémoire tampon, à l’exclusion du caractère null de fin.

</dd> <dt>

*lpType* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une variable qui reçoit un code indiquant le type de données stockées dans la valeur spécifiée. Pour obtenir la liste des codes de type possibles, consultez [types de valeurs de Registre](../sysinfo/registry-value-types.md). Le paramètre *lpType* peut avoir la **valeur null** si le code de type n’est pas requis.

</dd> <dt>

*lpData* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit les données de l’entrée de valeur. Ce paramètre peut avoir la **valeur null** si les données ne sont pas requises.

Si *lpData* a la **valeur null** et que *LpcbData* n’a pas la **valeur null**, la fonction stocke la taille des données, en octets, dans la variable vers laquelle pointe *lpcbData*. Cela permet à une application de déterminer la meilleure façon d’allouer une mémoire tampon pour les données.

</dd> <dt>

*lpcbData* \[ in, out, facultatif\]
</dt> <dd>

Pointeur vers une variable qui spécifie la taille de la mémoire tampon vers laquelle pointe le paramètre *lpData* , en octets. Lorsque la fonction retourne, la variable reçoit le nombre d’octets stockés dans la mémoire tampon.

Ce paramètre peut être **null** uniquement si *LpData* a la **valeur null**.

Si les données ont le \_ type reg SZ, \_ reg \_ multisz ou reg \_ expand \_ SZ, cette taille inclut tous les caractères null de fin. Pour plus d'informations, consultez la section Notes.

Si la mémoire tampon spécifiée par *lpData* n’est pas suffisamment grande pour contenir les données, la fonction retourne l’erreur \_ plus de \_ données et stocke la taille de mémoire tampon requise dans la variable vers laquelle pointe *lpcbData*. Dans ce cas, le contenu de *lpData* n’est pas défini.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h. Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.

Si la mémoire tampon *lpData* est trop petite pour recevoir la valeur, la fonction retourne l’erreur \_ plus de \_ données.

## <a name="remarks"></a>Notes

Pour énumérer des valeurs, une application doit appeler initialement la fonction **OREnumValue** avec le paramètre *dwIndex* défini sur zéro. L’application doit ensuite incrémenter *dwIndex* et appeler la fonction **OREnumValue** jusqu’à ce qu’il n’y ait plus de valeur (jusqu’à ce que la fonction retourne l’erreur plus \_ aucun \_ \_ élément).

L’application peut également définir *dwIndex* sur l’index de la dernière valeur sur le premier appel à la fonction et décrémenter l’index jusqu’à ce que la valeur avec l’index 0 soit énumérée. Pour récupérer l’index de la dernière valeur, utilisez la fonction [**ORQueryInfoKey**](orqueryinfokey.md) .

Lors de l’utilisation de **OREnumValue**, une application ne doit pas appeler de fonctions de Registre hors connexion qui peuvent modifier la clé en cours d’interrogation.

Si les données ont le \_ type reg SZ, \_ reg \_ multisz ou reg \_ expand \_ SZ, la chaîne n’a peut-être pas été stockée avec les caractères de fin null corrects. Par conséquent, même si la fonction retourne \_ une erreur, l’application doit s’assurer que la chaîne se termine correctement avant de l’utiliser ; sinon, elle peut remplacer une mémoire tampon. (Notez que REG \_ \_Les chaînes à plusieurs SZ doivent avoir deux caractères de fin null.)

Pour déterminer la taille maximale du nom et des tampons de données, utilisez la fonction [**ORQueryInfoKey**](orqueryinfokey.md) .

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

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORQueryInfoKey**](orqueryinfokey.md)
</dt> </dl>

 

 
