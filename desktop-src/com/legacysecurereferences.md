---
title: LegacySecureReferences
description: Détermine si les appels AddRef/Release sont sécurisés pour les applications qui n’appellent pas CoInitializeSecurity.
ms.assetid: 955b599b-1858-475a-95c4-a55038a28e69
keywords:
- Valeur de Registre LegacySecureReferences COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef3a4ab964d73fa4b194c734f28c23ff068239370088c090051464129b6caf14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736546"
---
# <a name="legacysecurereferences"></a>LegacySecureReferences

Détermine si les / appels de **version** de AddRef sont sécurisés pour les applications qui n’appellent pas [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacySecureReferences = value
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur de **reg \_ SZ** . La valeur « Y » ou « y » indiquent que **AddRef** et **Release** sont sécurisés. Si cette valeur de Registre est absente ou est définie sur une valeur autre que « Y » ou « y », **AddRef** et **Release** ne sont pas sécurisés. L’activation de références sécurisées ralentit les appels distants.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription des serveurs COM](registering-com-servers.md)
</dt> <dt>

[Définition de la sécurité au niveau du processus](setting-processwide-security.md)
</dt> </dl>

 

 




