---
description: La fonction CreateProtocol notifie Moniteur réseau qu’un analyseur de protocole spécifique existe.
ms.assetid: 13ae261f-b1c0-4afc-b718-d64b3d4ec5ee
title: CreateProtocol, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateProtocol
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 173f744406ef2b360c0af7158e397c2001f146b9f2339bf6aaf3468b9a1465dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796350"
---
# <a name="createprotocol-function"></a>CreateProtocol fonction)

La fonction **CreateProtocol** notifie Moniteur réseau qu’un analyseur de protocole spécifique existe.

## <a name="syntax"></a>Syntaxe


```C++
HPROTOCOL WINAPI CreateProtocol(
  _In_ LPSTR         ProtocolName,
  _In_ LPENTRYPOINTS lpEntryPoints,
  _In_ DWORD         cbEntryPoints
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ProtocolName* \[ dans\]
</dt> <dd>

Nom du protocole détecté par l’analyseur.

</dd> <dt>

*lpEntryPoints* \[ dans\]
</dt> <dd>

Structure [ENTRYPOINTS](entrypoints.md) qui contient les autres points d’entrée de la dll de l’analyseur. Consultez la section Notes pour obtenir la liste des fonctions d’exportation auxquelles chaque point d’entrée fait référence. Les points d’entrée doivent être fournis dans l’ordre spécifié par la structure **ENTRYPOINTS** .

</dd> <dt>

*cbEntryPoints* \[ dans\]
</dt> <dd>

Taille de la structure **ENTRYPOINTS** . Moniteur réseau fournit une \_ macro de taille ENTRYPOINTS que vous pouvez utiliser pour spécifier la taille de la structure.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est un handle vers le protocole.

Si la fonction échoue, la valeur de retour est **null**.

## <a name="remarks"></a>Remarques

La DLL de l’analyseur appelle **CreateProtocol** pendant son implémentation de [DllMain](dllmain-parser.md). La fonction **CreateProtocol** est appelée quand le système d’exploitation charge la dll de l’analyseur pour la première fois.

Les points d’entrée référencés dans le paramètre *lpEntryPoints* incluent des pointeurs vers les fonctions d’exportation suivantes qui doivent être fournies dans l’ordre présenté ici.

-   [S’inscrire](register-parser.md)
-   [Désinscrire](deregister.md)
-   [RecognizeFrame](recognizeframe.md)
-   [AttachProperties](attachproperties.md)
-   [FormatProperties](formatproperties.md)



| Pour plus d’informations sur                                                                                 | Consultez                                                     |
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| Ce que sont les analyseurs et comment ils fonctionnent avec Moniteur réseau.                                          | [Analyseurs](parsers.md)                                  |
| La procédure d’implémentation de **DllMain** comprend un exemple d’appel de **CreateProtocol** dans **DllMain**. | [Implémentation de DllMain](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[DllMain](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

