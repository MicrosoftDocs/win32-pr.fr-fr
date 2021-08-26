---
description: GetOwnerSid&\# 8194 ; La méthode de classe WMI récupère l’identificateur de sécurité (SID) pour le propriétaire de ce processus.
ms.assetid: f856b06c-8080-4145-a775-51361f741873
ms.tgt_platform: multiple
title: Méthode GetOwnerSid de la classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwnerSid
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2884c0f1cd3cc6e32a2db1ab14824ba3112624002cb10f4d76782d622e069000
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918379"
---
# <a name="getownersid-method-of-the-win32_process-class"></a>Méthode GetOwnerSid de la \_ classe de processus Win32

La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **GetOwnerSid** récupère l’identificateur de sécurité (SID) pour le propriétaire de ce processus.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetOwnerSid(
  [out] string Sid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Sid* \[ à\]
</dt> <dd>

Retourne le descripteur d’identificateur de sécurité pour ce processus.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne zéro (0) pour indiquer la réussite de l’opération. Tout autre nombre indique une erreur. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Achèvement réussi** (0)
</dt> <dt>

**Accès refusé** (2)
</dt> <dt>

**Privilèges insuffisants** (3)
</dt> <dt>

**Échec inconnu** (8)
</dt> <dt>

**Chemin introuvable** (9)
</dt> <dt>

**Paramètre non valide** (21)
</dt> <dt>

**Autre** (22 4294967295)
</dt> </dl>

## <a name="examples"></a>Exemples

L’exemple de code de [recherche des utilisateurs connectés sur un système distant/s version 2](https://Gallery.TechNet.Microsoft.Com/Find-the-logged-on-users-1161bd92) PowerShell interroge les ordinateurs distants pour voir qui est connecté.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Processus Win32**](win32-process.md)
</dt> </dl>

 

