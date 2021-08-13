---
description: Exclut les disques de l’opération Autochk à exécuter au redémarrage suivant.
ms.assetid: 5df2bc3b-e149-4853-aa02-af4cb8af6da0
ms.tgt_platform: multiple
title: Méthode ExcludeFromAutochk de la classe Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ExcludeFromAutochk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a37171c594cb3a51b131220bb604234bcae108fa025ea6343da99fdc998a7dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118676127"
---
# <a name="excludefromautochk-method-of-the-win32_logicaldisk-class"></a>Méthode ExcludeFromAutochk de la \_ classe disque logique Win32

La méthode **ExcludeFromAutochk** exclut les disques de l’opération **Autochk** à exécuter au redémarrage suivant.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 ExcludeFromAutochk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Disque logique* \[ dans\]
</dt> <dd>

Liste des lecteurs qui doivent être exclus de **Autochk** au prochain redémarrage. La syntaxe de chaîne se compose de la lettre de lecteur suivie d’un signe deux-points pour le disque logique.

Exemple : "C :"

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur 0 (zéro) quand aucune erreur ne se produit. Les valeurs sont répertoriées dans la liste suivante. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Opération réussie** (0)
</dt> <dt>

**Erreur : lecteur distant** (1)
</dt> <dt>

**Erreur : lecteur amovible** (2)
</dt> <dt>

**Erreur : le lecteur n’est pas un répertoire racine** (3)
</dt> <dt>

**Erreur : lecteur inconnu** (4)
</dt> </dl>

## <a name="remarks"></a>Remarques

S’il n’est pas exclu, **Autochk** est exécuté sur le disque lorsque le bit d’intégrité est défini pour le disque. Notez que les appels pour exclure des disques ne sont pas cumulatifs. Si un appel est effectué pour exclure certains disques, la nouvelle liste n’est pas ajoutée à la liste des disques déjà marqués pour l’exclusion. La nouvelle liste de disques remplace la liste précédente. Cette méthode s’applique uniquement aux instances de disque logique qui représentent un disque physique de l’ordinateur. Elle ne s’applique pas aux lecteurs logiques mappés.

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant garantit que Autochk.exe ne s’exécutera pas sur le lecteur C lors du prochain redémarrage de l’ordinateur, même si le « bit d’intégrité » a été défini sur le lecteur C.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ExcludeFromAutoChk(Array("C:")) 
```



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

[**\_Disque logique Win32**](win32-logicaldisk.md)
</dt> <dt>

[Classes matérielles du système informatique](computer-system-hardware-classes.md)
</dt> </dl>

 

