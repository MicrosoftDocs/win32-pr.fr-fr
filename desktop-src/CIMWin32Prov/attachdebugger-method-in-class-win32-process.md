---
description: Démarre le débogueur actuellement inscrit pour ce processus.
ms.assetid: 63c30db8-6117-4353-9132-4f39c72a6637
ms.tgt_platform: multiple
title: Méthode AttachDebugger de la classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.AttachDebugger
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 041bdeeab634ebed5c7ec2eccffe01f7cecce709
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414017"
---
# <a name="attachdebugger-method-of-the-win32_process-class"></a>Méthode AttachDebugger de la \_ classe de processus Win32

La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **AttachDebugger** démarre le débogueur actuellement inscrit pour ce processus.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 AttachDebugger();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs répertoriées dans la liste suivante ou toute autre valeur pour indiquer une erreur. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Opération réussie**
</dt> <dd>

0

Achèvement réussi.

</dd> <dt>

**Accès refusé**
</dt> <dd>

2

L’utilisateur n’a pas accès aux informations demandées.

</dd> <dt>

**Privilège insuffisant**
</dt> <dd>

3

L’utilisateur ne dispose pas de privilèges suffisants.

</dd> <dt>

**Échec inconnu**
</dt> <dd>

8

Échec inconnu.

</dd> <dt>

**Chemin d'accès introuvable**
</dt> <dd>

9

Le chemin d'accès spécifié n'existe pas.

</dd> <dt>

**Paramètre non valide**
</dt> <dd>

21

Le paramètre spécifié n’est pas valide.

</dd> <dt>

**Autres**
</dt> <dd>

22 4294967295

</dd> </dl>

## <a name="requirements"></a>Spécifications



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

 

