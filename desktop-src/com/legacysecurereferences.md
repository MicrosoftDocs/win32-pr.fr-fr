---
title: LegacySecureReferences
description: Détermine si les appels AddRef/Release sont sécurisés pour les applications qui n’appellent pas CoInitializeSecurity.
ms.assetid: 955b599b-1858-475a-95c4-a55038a28e69
keywords:
- Valeur de Registre LegacySecureReferences COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2776bf3661013f1e622bbc2e1c553f2551c62808
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293675"
---
# <a name="legacysecurereferences"></a>LegacySecureReferences

Détermine si les / appels de **version** de AddRef sont sécurisés pour les applications qui n’appellent pas [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacySecureReferences = value
```

## <a name="remarks"></a>Notes

Il s’agit d’une valeur de **reg \_ SZ** . La valeur « Y » ou « y » indiquent que **AddRef** et **Release** sont sécurisés. Si cette valeur de Registre est absente ou est définie sur une valeur autre que « Y » ou « y », **AddRef** et **Release** ne sont pas sécurisés. L’activation de références sécurisées ralentit les appels distants.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription des serveurs COM](registering-com-servers.md)
</dt> <dt>

[Définition de la sécurité au niveau du processus](setting-processwide-security.md)
</dt> </dl>

 

 




