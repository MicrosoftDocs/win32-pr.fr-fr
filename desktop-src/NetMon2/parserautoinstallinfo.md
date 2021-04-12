---
description: La fonction d’exportation ParserAutoInstallInfo identifie l’analyseur, ou les analyseurs qui se trouvent dans une DLL. ParserAutoInstallInfo doit être implémenté dans toutes les dll de l’analyseur.
ms.assetid: 7af3bf3c-d415-4af9-8f5c-c9a76535bd1a
title: Fonction de rappel ParserAutoInstallInfo (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParserAutoInstallInfo
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 7702ae8aad5ae24acf3835451b7b8eff3a26ceb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318073"
---
# <a name="parserautoinstallinfo-callback-function"></a>ParserAutoInstallInfo fonction de rappel

La fonction d’exportation **ParserAutoInstallInfo** identifie l’analyseur, ou les analyseurs qui se trouvent dans une dll. **ParserAutoInstallInfo** doit être implémenté dans toutes les dll de l’analyseur.

## <a name="syntax"></a>Syntaxe


```C++
PPF_PARSERDLLINFO WINAPI ParserAutoInstallInfo(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction de rappel n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une structure [ \_ PARSERDLLINFO de PF](pf-parserdllinfo.md) qui décrit les analyseurs dans la dll.

Si la fonction échoue, la valeur de retour est **false**.

## <a name="remarks"></a>Notes

Lorsque Moniteur réseau se charge pour la première fois, il appelle **ParserAutoInstallInfo** (s’il existe) pour installer automatiquement chaque analyseur, puis énumère toutes les dll de l’analyseur dans le sous-répertoire de l’analyseur.

Les informations retournées dans la structure **\_ PARSERDLLINFO de PF** incluent les éléments suivants :

-   Nombre d’analyseurs dans la DLL (en général, un).
-   Le nom et une brève description du protocole détecté par chaque analyseur.
-   Fichier d’aide facultatif pour chaque protocole.
-   Les protocoles qui précèdent chaque protocole.
-   Les protocoles qui suivent chaque protocole.

Chaque DLL de l’analyseur doit contenir un analyseur. Toutefois, Moniteur réseau vous permet de créer une DLL qui contient plus d’un analyseur. Par exemple, tcpip.dll est une Moniteur réseau DLL avec plus d’un analyseur.



| Pour plus d’informations sur                                               | Consultez                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| Ce que sont les analyseurs et comment ils fonctionnent avec Moniteur réseau.        | [Analyseurs](parsers.md)                                                       |
| Les points d’entrée inclus dans la DLL de l’analyseur.               | [Architecture des DLL de l’analyseur](parser-dll-architecture.md)                       |
| L’implémentation de **ParserAutoInstallInfo**  comprend un exemple. | [Implémentation de ParserAutoInstallInfo](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[\_PARSERDLLINFO PF](pf-parserdllinfo.md)
</dt> </dl>

 

 




