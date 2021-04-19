---
description: La fonction d’exportation AttachProperties mappe les propriétés à un emplacement dans une partie des données reconnues. AttachProperties doit être implémenté pour chaque analyseur pris en charge par la DLL de l’analyseur.
ms.assetid: ef28f571-8364-47d0-841c-580e89333afd
title: Fonction de rappel AttachProperties (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 3b3cb4be93b8d960b39f0f5c5cf2b5a4809573cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533875"
---
# <a name="attachproperties-callback-function"></a>AttachProperties fonction de rappel

La fonction d’exportation **AttachProperties** mappe les propriétés à un emplacement dans une partie des données reconnues. **AttachProperties** doit être implémenté pour chaque analyseur pris en charge par la dll de l’analyseur.

## <a name="syntax"></a>Syntaxe


```C++
DWORD AttachProperties(
  _In_ HFRAME    hFrame,
  _In_ LPBYTE    lpFrame,
  _In_ LPBYTE    lpProtocol,
  _In_ DWORD     MacType,
  _In_ DWORD     BytesLeft,
  _In_ HPROTOCOL hPreviousProtocol,
  _In_ DWORD     nPreviousProtocolOffset,
  _In_ DWORD     lpInstData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFrame* \[ dans\]
</dt> <dd>

Handle du frame en cours d’analyse.

</dd> <dt>

*lpFrame* \[ dans\]
</dt> <dd>

Pointeur vers le premier octet d’un frame.

</dd> <dt>

*lpProtocol* \[ dans\]
</dt> <dd>

Pointeur vers le début des données reconnues.

</dd> <dt>

*MacType* \[ dans\]
</dt> <dd>

Valeur MAC du premier protocole dans un frame. Le *paractype* peut être l’un des suivants :



| Valeur                                                                                                                                                                         | Signification                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <dt>**MAC \_ type \_ Ethernet**</dt> </dl>    | 802.3 <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <dt>**\_type Mac \_ TOKENRING**</dt> </dl> | 802.5 <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <dt>**\_type Mac \_ FDDI**</dt> </dl>                | ANSI X3T 9.5 <br/> |



 

</dd> <dt>

*BytesLeft* \[ dans\]
</dt> <dd>

Nombre d’octets restants dans un frame à partir du début des données reconnues.

</dd> <dt>

*hPreviousProtocol* \[ dans\]
</dt> <dd>

Handle du protocole précédent.

</dd> <dt>

*nPreviousProtocolOffset* \[ dans\]
</dt> <dd>

Décalage du protocole précédent à partir du début du frame.

</dd> <dt>

*lpInstData* \[ dans\]
</dt> <dd>

Pointeur vers les données d’instance fournies par le protocole précédent. La longueur des données d’instance ne peut pas être supérieure à celle \_ d’un PTR DWORD.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est un pointeur vers le premier octet après les données reconnues dans un frame ou **null** si les données reconnues sont la dernière partie des données d’un frame.

Si la fonction échoue, la valeur de retour est un pointeur vers les données reconnues. Le paramètre *lpProtocol* passe le pointeur à la dll de l’analyseur.

## <a name="remarks"></a>Notes

Moniteur réseau appelle la fonction **AttachProperties** pour chaque analyseur qui reconnaît un élément de données dans un frame. Notez que l’analyseur détermine les propriétés qui existent dans les données reconnues, ainsi que l’emplacement de chaque propriété.

Pendant l’implémentation de **AttachProperties**, appelez [AttachPropertyInstance](attachpropertyinstance.md) pour utiliser les données telles qu’elles existent dans la capture. Vous pouvez également appeler la fonction [AttachPropertyInstanceEx](attachpropertyinstanceex.md) pour modifier les données de propriété. Toutefois, il est recommandé d’utiliser les données telles qu’elles existent dans la capture.

Les fonctions **AttachPropertyInstanceEx** et **AttachPropertyInstance** sont appelées uniquement pour les propriétés qui existent dans les données reconnues. Notez que Moniteur réseau a une [*base de données de propriétés*](p.md) pour l’analyseur qui contient une description de toutes les propriétés prises en charge par l’analyseur.

**Données d’instance**

Les données d’instance sont des informations transmises d’un analyseur à un autre. Les données d’instance peuvent être des données qui sont inférieures ou égales à un \_ ptr DWORD en longueur, ou un pointeur vers des données, telles que des données de trame brutes, qui n’a pas besoin d’être alloué ou libéré par l’analyseur. Dans le paramètre *lpInstData* des fonctions **AttachProperties** et [RecognizeFrame](recognizeframe.md) , moniteur réseau fournit un pointeur vers les données d’instance du protocole précédent. Vous pouvez définir les données d’instance de votre analyseur lors de l’implémentation de **RecognizeFrame**.



| Pour plus d’informations sur                                          | Consultez                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| Ce que sont les analyseurs et comment ils fonctionnent avec Moniteur réseau.   | [Analyseurs](parsers.md)                                             |
| Les points d’entrée inclus dans la DLL de l’analyseur.           | [Architecture des DLL de l’analyseur](parser-dll-architecture.md)             |
| Comment reconnaître des données.                                      | [Implémentation de RecognizeFrame](implementing-recognizeframe.md)     |
| Comment créer une base de données de propriétés.                          | [Implémentation du Registre](implementing-register.md)                 |
| L’implémentation de **AttachProperties**  comprend un exemple. | [Implémentation de AttachProperties](implementing-attachproperties.md) |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[AttachPropertyInstance](attachpropertyinstance.md)
</dt> <dt>

[AttachPropertyInstanceEx](attachpropertyinstanceex.md)
</dt> <dt>

[RecognizeFrame](recognizeframe.md)
</dt> </dl>

 

 




