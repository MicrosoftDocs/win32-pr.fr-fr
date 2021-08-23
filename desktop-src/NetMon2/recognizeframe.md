---
description: La fonction d’exportation RecognizeFrame indique si un élément de données est reconnu comme le protocole détecté par l’analyseur. La fonction d’exportation RecognizeFrame doit être implémentée pour chaque analyseur pris en charge par la DLL de l’analyseur.
ms.assetid: 3f835f58-b011-4329-b9b2-ff865a1f0ae5
title: Fonction de rappel RecognizeFrame (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognizeFrame
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: b9f8fcbfccdb306038b7b654e947ff1a11654267012c7527799d8633ed8a9410
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889699"
---
# <a name="recognizeframe-callback-function"></a>RecognizeFrame fonction de rappel

La fonction d’exportation **RecognizeFrame** indique si un élément de données est reconnu comme le protocole détecté par l’analyseur. La fonction d’exportation **RecognizeFrame** doit être implémentée pour chaque analyseur pris en charge par la dll de l’analyseur.

## <a name="syntax"></a>Syntaxe


```C++
LPBYTE RecognizeFrame(
  _In_    HFRAME      hFrame,
  _In_    LPBYTE      lpFrame,
  _In_    LPBYTE      lpProtocol,
  _In_    DWORD       MacType,
  _In_    DWORD       BytesLeft,
  _In_    HPROTOCOL   hPreviousProtocol,
  _In_    DWORD       nPreviousProtocolOffset,
  _Out_   LPDWORD     ProtocolStatusCode,
  _Out_   LPHPROTOCOL phNextProtocol,
  _Inout_ PDWORD_PTR  lpInstData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFrame* \[ dans\]
</dt> <dd>

Handle vers le frame qui contient les données.

</dd> <dt>

*lpFrame* \[ dans\]
</dt> <dd>

Pointeur vers le premier octet d’un frame. Le pointeur fournit un moyen d’afficher les données que les autres analyseurs reconnaissent.

</dd> <dt>

*lpProtocol* \[ dans\]
</dt> <dd>

Pointeur vers le début des données inrécupérées. En règle générale, les données non réclamées se trouvent au milieu d’une trame, car un analyseur précédent a demandé des données avant cet analyseur. L’analyseur doit d’abord tester les données non réclamées.

</dd> <dt>

*MacType* \[ dans\]
</dt> <dd>

Valeur MAC du premier protocole dans un frame. En règle générale, la valeur *MacType* est utilisée lorsque l’analyseur doit identifier le premier protocole dans un frame. La valeur *MacType* peut être l’une des suivantes :



| Valeur                                                                                                                                                                         | Signification                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <dt>**MAC \_ type \_ Ethernet**</dt> </dl>    | 802.3 <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <dt>**\_type Mac \_ TOKENRING**</dt> </dl> | 802.5 <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <dt>**\_type Mac \_ FDDI**</dt> </dl>                | ANSI X3T 9.5 <br/> |



 

</dd> <dt>

*BytesLeft* \[ dans\]
</dt> <dd>

Nombre d’octets restants à partir d’un emplacement dans un frame jusqu’à la fin du frame.

</dd> <dt>

*hPreviousProtocol* \[ dans\]
</dt> <dd>

Handle du protocole précédent.

</dd> <dt>

*nPreviousProtocolOffset* \[ dans\]
</dt> <dd>

Décalage du début du protocole précédent du frame.

</dd> <dt>

*ProtocolStatusCode* \[ à\]
</dt> <dd>

Indicateur d’état de protocole. La DLL de l’analyseur doit définir l’un des codes d’état suivants.



| Valeur                                                                                                                                                                                                              | Signification                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROTOCOL_STATUS_RECOGNIZED"></span><span id="protocol_status_recognized"></span><dl> <dt>**État du protocole \_ \_ reconnu**</dt> </dl>              | L’analyseur reconnaît les données, mais ne sait pas quel protocole suit. Après avoir défini le code, retournez un pointeur vers les données non réclamées restantes qui suivent le protocole reconnu. Moniteur réseau utilise le [*jeu suivant*](f.md) du protocole pour poursuivre l’analyse. <br/> |
| <span id="PROTOCOL_STATUS_NOT_RECOGNIZED"></span><span id="protocol_status_not_recognized"></span><dl> <dt>**État du protocole \_ \_ non \_ reconnu**</dt> </dl> | L’analyseur ne reconnaît pas les données. Après avoir défini ce code, retournez le pointeur au début des données à l’aide du pointeur que le paramètre *lpProtocol* transmet à la dll de l’analyseur. Moniteur réseau utilise le *jeu suivant* du protocole précédent pour poursuivre l’analyse. <br/>                |
| <span id="PROTOCOL_STATUS_CLAIMED"></span><span id="protocol_status_claimed"></span><dl> <dt>**État du protocole \_ \_ demandé**</dt> </dl>                       | L’analyseur reconnaît les données et prétend les données restantes. Après avoir défini le code, retournez **null** pour moniteur réseau pour terminer l’analyse d’un frame. <br/>                                                                                                                                           |
| <span id="PROTOCOL_STATUS_NEXT_PROTOCOL"></span><span id="protocol_status_next_protocol"></span><dl> <dt>**\_ \_ protocole suivant de l’état du protocole \_**</dt> </dl>    | L’analyseur reconnaît les données et sait quel protocole suit. Après avoir défini le code, définissez le paramètre *phNextProtocol* et retournez un pointeur vers les données non réclamées restantes qui suivent le protocole reconnu. Moniteur réseau poursuit l’analyse du frame. <br/>                               |



 

</dd> <dt>

*phNextProtocol* \[ à\]
</dt> <dd>

Pointeur vers le handle du protocole suivant. Ce paramètre est défini lorsqu’un protocole identifie le protocole qui suit un protocole. Pour obtenir le descripteur du protocole suivant, appelez la fonction [GetProtocolFromTable](getprotocolfromtable.md) .

</dd> <dt>

*lpInstData* \[ in, out\]
</dt> <dd>

En entrée, pointeur vers les données d’instance du protocole précédent.

Lors de la sortie, pointeur vers les données d’instance pour le protocole en cours. La longueur des données d’instance ne peut pas être supérieure à celle \_ d’un PTR DWORD.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est un pointeur vers le premier octet après les données de l’analyseur reconnues. Si l’analyseur prétend toutes les données restantes, la valeur de retour est **null**.

Si la fonction échoue, la valeur de retour est un pointeur initial que le paramètre *lpProtocol* passe.

## <a name="remarks"></a>Remarques

La fonction **RecognizeFrame** détermine si l’analyseur reconnaît les données brutes en commençant au pointeur *lpProtocol* .

-   Si le protocole reconnaît les données, la fonction **RecognizeFrame** retourne un pointeur vers les données restantes, ou retourne la **valeur null** si le protocole actuel est le dernier protocole dans un frame.
-   Si le protocole ne reconnaît pas les données, la fonction **RecognizeFrame** retourne le pointeur passé à la dll de l’analyseur dans le paramètre *lpProtocol* .

> [!Note]  
> *RecognizeFrame* peut être appelé avant que la fonction [*Register*](register-parser.md) soit appelée pour enregistrer les propriétés de protocole. Pour cette raison, l’implémentation de la fonction *RecognizeFrame* ne repose sur aucune propriété ou structure qui est créée ou initialisée pendant l’implémentation de la fonction de **registre** de protocole.

 

**Jeu de remise et ensemble de suivi**

Un analyseur peut utiliser un jeu de remise ou un ensemble de suivi pour identifier les Moniteur réseau le protocole qui suit les données reconnues.

-   Si des informations sont disponibles dans les données reconnues, l’analyseur utilise son jeu de remise pour obtenir un handle pour le protocole suivant, puis passe ce handle à Moniteur réseau.
-   Si aucune information n’est disponible, l’analyseur ne passe pas de handle et Moniteur réseau utilise le jeu de suivi de l’analyseur pour déterminer le protocole qui suit.

**Passage d’informations entre les protocoles**

Utilisez le paramètre *lpInstData* pour transmettre des informations entre les protocoles. En entrée, vous pouvez récupérer les informations du protocole précédent. Lors de la sortie, vous pouvez transmettre des informations au protocole suivant.

Les données d’instance peuvent être des données qui sont inférieures ou égales à un \_ ptr DWORD en longueur, ou un pointeur vers des données, telles que des données de trame brutes, qui n’a pas besoin d’être alloué ou libéré par l’analyseur.



| Pour plus d’informations sur                                        | Consultez                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Ce que sont les analyseurs et comment ils fonctionnent avec Moniteur réseau. | [Analyseurs](parsers.md)                                                                                                    |
| Les points d’entrée inclus dans la DLL de l’analyseur.        | [Architecture des DLL de l’analyseur](parser-dll-architecture.md)                                                                    |
| L’implémentation de **RecognizeFrame**  comprend un exemple. | [Implémentation de RecognizeFrame](implementing-recognizeframe.md)                                                            |
| Comment spécifier un jeu de remise et un ensemble de suivi.              | [Spécification d’un jeu de remise](specifying-a-handoff-set.md)[spécifiant un ensemble suivant](specifying-a-follow-set.md)<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[GetProtocolFromTable](getprotocolfromtable.md)
</dt> </dl>

 

 




