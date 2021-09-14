---
description: Décompresse le fichier de données logique (ou le répertoire) qui est spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode decompress et est héritée de la \_ LOGICALFILE CIM.
ms.assetid: 30b62930-1d4a-47c0-8b57-b460edb5dbd0
ms.tgt_platform: multiple
title: Méthode UncompressEx de la classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0d11585a834ecc357447394ce09b73698bf2de86
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006854"
---
# <a name="uncompressex-method-of-the-cim_datafile-class"></a>Méthode UncompressEx de la \_ classe de fichier de fichier CIM

La méthode **UncompressEx** décompresse le fichier de données logique (ou le répertoire) qui est spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode [**decompress**](uncompress-method-in-class-cim-datafile.md) et est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 UncompressEx(
  [out] string  StopFileName,
  [in]  string  StartFileName,
  [in]  boolean Recursive
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StopFileName* \[ à\]
</dt> <dd>

Nom du fichier (ou répertoire) dans lequel la méthode a échoué. Ce paramètre a la **valeur null** si la méthode est réussie.

</dd> <dt>

*StartFileName* \[ dans\]
</dt> <dd>

Fichier enfant (ou répertoire) à utiliser comme point de départ pour cette méthode. En règle générale, le paramètre *StartFileName* est le paramètre *StopFileName* spécifiant le fichier (ou le répertoire) auquel une erreur s’est produite à partir de l’appel de méthode précédent. Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier (ou le répertoire) spécifié dans l’appel de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .

Si *il* est utilisé, la valeur *recursive* doit également être définie sur true.

</dd> <dt>

*Récursif* \[ dans\]
</dt> <dd>

Si la **valeur est true**, la méthode est également appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance du fichier de [**\_ fichier CIM**](cim-datafile.md) . Pour les instances de fichier, ce paramètre est ignoré.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Réussite.

</dd> <dt>

**2**
</dt> <dd>

Accès refusé.

</dd> <dt>

**8**
</dt> <dd>

Échec non spécifié.

</dd> <dt>

**9**
</dt> <dd>

Objet non valide.

</dd> <dt>

**10**
</dt> <dd>

L’objet existe déjà.

</dd> <dt>

**11**
</dt> <dd>

Le système de fichiers n’est pas NTFS.

</dd> <dt>

**12**
</dt> <dd>

Plateforme non Windows.

</dd> <dt>

**13**
</dt> <dd>

Le lecteur n’est pas le même.

</dd> <dt>

**14**
</dt> <dd>

le répertoire n'est pas vide.

</dd> <dt>

**15**
</dt> <dd>

Violation de partage.

</dd> <dt>

**16**
</dt> <dd>

Fichier de démarrage non valide.

</dd> <dt>

**17**
</dt> <dd>

Privilège non détenu.

</dd> <dt>

**21**
</dt> <dd>

Paramètre non valide.

</dd> </dl>

## <a name="remarks"></a>Notes

La méthode **UncompressEx** dans le [**fichier de \_ fichier CIM**](cim-datafile.md) est implémentée par WMI.

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

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

[**\_Fichier de fichier CIM**](uncompressex-method-in-class-cim-datafile.md)
</dt> <dt>

[**\_Fichier de fichier CIM**](cim-datafile.md)
</dt> <dt>

[Tâches WMI : fichiers et dossiers](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Constantes de droits d’accès aux fichiers et aux répertoires**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

