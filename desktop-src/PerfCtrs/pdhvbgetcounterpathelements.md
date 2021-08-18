---
description: La fonction PdhVbGetCounterPathElements analyse une chaîne de chemin d’accès au compteur de performance complet dans ses éléments individuels.
ms.assetid: 5459c7dd-e8b6-48cd-a33f-cafdc64dd9ee
title: PdhVbGetCounterPathElements fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetCounterPathElements
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: fecd9ecac573ecc1a5afabcfc4a14bf6fd1ca5cee7b44387ea910b0cf1a5820d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011327"
---
# <a name="pdhvbgetcounterpathelements-function"></a>PdhVbGetCounterPathElements fonction)

La fonction **PdhVbGetCounterPathElements** analyse une chaîne de chemin d’accès au compteur de performance complet dans ses éléments individuels. Chacune des variables de chaîne doit avoir la même taille (*bufferSize*) et être dimensionnée et initialisée avant d’être utilisée dans cette fonction.

> [!IMPORTANT]
> La fonction décrite dans cette rubrique peut être modifiée ou non disponible à l’avenir. Au lieu de cela, Microsoft vous recommande d’utiliser les fonctions décrites dans [fonctions des compteurs de performances](performance-counters-functions.md).

Function PdhVbGetCounterPathElements ( \_ ByVal PathString As String, \_ ByVal MachineName As String, \_ ByVal ObjectName As String, \_ ByVal InstanceName As String, \_ ByVal ParentInstance As String, \_ ByVal CounterName As String, \_ ByVal bufferSize As long \_ ) As long

## <a name="parameters"></a>Paramètres

<dl> <dt>

*PathString* 
</dt> <dd>

Chaîne du chemin d’accès du compteur qui doit être divisée en ses éléments individuels.

</dd> <dt>

*MachineName* 
</dt> <dd>

Chaîne devant recevoir le nom de l’ordinateur.

</dd> <dt>

*ObjectName* 
</dt> <dd>

Chaîne devant recevoir le nom de l’objet.

</dd> <dt>

*InstanceName* 
</dt> <dd>

Chaîne devant recevoir le nom de l’instance, s’il est utilisé.

</dd> <dt>

*ParentInstance* 
</dt> <dd>

Chaîne devant recevoir l’instance parente, si elle est utilisée.

</dd> <dt>

*CounterName* 
</dt> <dd>

Chaîne qui reçoit le nom du compteur.

</dd> <dt>

*BufferSize* 
</dt> <dd>

Taille maximale de chaque variable de chaîne utilisée en tant que paramètre pour cet appel de fonction.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, elle retourne un entier **long** égal à la réussite de l’erreur \_ .

Si la fonction échoue, la valeur de retour est un [code d’erreur système](/windows/desktop/Debug/system-error-codes) ou un [code d’erreur PDH](pdh-error-codes.md). Les valeurs possibles sont les suivantes.



| Code de retour                                                                                                     | Description                                                                                    |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>**PDH \_ argument non valide \_**</dt> </dl>           | Une ou plusieurs des mémoires tampons de chaîne n’ont pas la taille correcte.<br/>                          |
| <dl> <dt>**PDH \_ \_ données supplémentaires**</dt> </dl>                  | Un ou plusieurs éléments du chemin d’accès du compteur sont trop volumineux pour la longueur de la mémoire tampon de retour.<br/> |
| <dl> <dt>**\_échec d' \_ allocation de mémoire PDH \_**</dt> </dl> | Impossible d’allouer une mémoire tampon temporaire.<br/>                                   |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| Bibliothèque<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

