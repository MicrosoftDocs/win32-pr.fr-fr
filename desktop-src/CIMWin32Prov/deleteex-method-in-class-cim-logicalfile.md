---
description: La méthode DeleteEx supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode Delete.
ms.assetid: 53785f2e-8796-446c-8228-9abc2d9a0d68
ms.tgt_platform: multiple
title: Méthode DeleteEx de la classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4f9799513111ff53bb97c14feaf70c922dfb085
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523399"
---
# <a name="deleteex-method-of-the-cim_logicalfile-class"></a>Méthode DeleteEx de la \_ classe CIM LogicalFile

La méthode **DeleteEx** supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode [**Delete**](delete-method-in-class-cim-logicalfile.md) .

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 DeleteEx(
  [out]          string StopFileName,
  [in, optional] string StartFileName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StopFileName* \[ à\]
</dt> <dd>

Chaîne qui représente le nom du fichier (ou répertoire) dans lequel la méthode a échoué. Ce paramètre a la valeur null si la méthode est réussie.

</dd> <dt>

*StartFileName* \[ dans, facultatif\]
</dt> <dd>

Chaîne qui nomme le fichier enfant (ou le répertoire) à utiliser comme point de départ de la méthode. En général, ce paramètre est le paramètre *StopFileName* spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent. Si ce paramètre a la valeur null, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.

<dl> <dt>

**Success**
</dt> <dd>

0

Réussite.

</dd> <dt>

**Accès refusé**
</dt> <dd>

2

Accès refusé.

</dd> <dt>

**Échec non spécifié**
</dt> <dd>

8

Échec non spécifié.

</dd> <dt>

**Objet non valide**
</dt> <dd>

9

Objet non valide.

</dd> <dt>

**L’objet existe déjà**
</dt> <dd>

10

L’objet existe déjà.

</dd> <dt>

**Système de fichiers non NTFS**
</dt> <dd>

11

Le système de fichiers n’est pas NTFS.

</dd> <dt>

**Plateforme non NT/Windows 2000**
</dt> <dd>

12

Plateforme non Windows.

</dd> <dt>

**Le lecteur n’est pas le même**
</dt> <dd>

13

Le lecteur n’est pas le même.

</dd> <dt>

**Répertoire non vide**
</dt> <dd>

14

le répertoire n'est pas vide.

</dd> <dt>

**Violation de partage**
</dt> <dd>

15

Violation de partage.

</dd> <dt>

**Fichier de démarrage non valide**
</dt> <dd>

16

Fichier de démarrage non valide.

</dd> <dt>

**Privilège non détenu**
</dt> <dd>

17

Privilège non détenu.

</dd> <dt>

**Paramètre non valide**
</dt> <dd>

21

Paramètre non valide.

</dd> </dl>

## <a name="remarks"></a>Notes

Actuellement, cette méthode n’est pas implémentée par WMI. Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

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

[\_LOGICALFILE CIM](deleteex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[**\_LOGICALFILE CIM**](cim-logicalfile.md)
</dt> </dl>

 

