---
description: Obtient la propriété du fichier d’entrée de répertoire logique spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode TakeOwnerShip et est héritée de CIM \_ LogicalFile.
ms.assetid: a13acaa2-2203-470a-b989-15f8276e46c6
ms.tgt_platform: multiple
title: Méthode TakeOwnerShipEx de la classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b02a6c40e99405c150a372f8eb15fe648f2df60a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127225289"
---
# <a name="takeownershipex-method-of-the-cim_directory-class"></a>Méthode TakeOwnerShipEx de la \_ classe de répertoire CIM

La méthode **TakeOwnerShipEx** obtient la propriété du fichier d’entrée de répertoire logique spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode [**TakeOwnership**](takeownership-method-in-class-cim-directory.md) et est héritée de [**CIM \_ LogicalFile**](cim-logicalfile.md). Si le fichier logique est un répertoire, cette méthode agit de manière récursive, en prenant possession de tous les fichiers et sous-répertoires contenus dans le répertoire.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 TakeOwnerShipEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StopFileName* \[ à\]
</dt> <dd>

Chaîne qui représente le nom du fichier (ou répertoire) dans lequel la méthode a échoué. Ce paramètre a la valeur null si la méthode est réussie.

</dd> <dt>

*StartFileName* \[ dans\]
</dt> <dd>

Chaîne qui représente le fichier enfant (ou le répertoire) à utiliser comme point de départ pour cette méthode. En général, ce paramètre est le paramètre *StopFileName* qui spécifie le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent. Si ce paramètre a la valeur null, l’opération est effectuée sur le fichier (ou le répertoire) spécifié dans l’appel de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .

</dd> <dt>

*Récursif* \[ dans\]
</dt> <dd>

Si la **valeur est true**, la méthode est appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance de [**\_ répertoire CIM**](cim-directory.md) . Pour les instances de fichier, ce paramètre est ignoré.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la valeur 0 en cas de réussite, et tout autre nombre pour indiquer une erreur.

<dl> <dt>


</dt> <dd>

0

Réussite.

</dd> <dt>


</dt> <dd>

2

Accès refusé.

</dd> <dt>


</dt> <dd>

8

Échec non spécifié.

</dd> <dt>


</dt> <dd>

9

Objet non valide.

</dd> <dt>


</dt> <dd>

10

L’objet existe déjà.

</dd> <dt>


</dt> <dd>

11

Le système de fichiers n’est pas NTFS.

</dd> <dt>


</dt> <dd>

12

La plateforme n’est pas Windows.

</dd> <dt>


</dt> <dd>

13

Le lecteur n’est pas le même.

</dd> <dt>


</dt> <dd>

14

le répertoire n'est pas vide.

</dd> <dt>


</dt> <dd>

15

Violation de partage.

</dd> <dt>


</dt> <dd>

16

Fichier de démarrage non valide.

</dd> <dt>


</dt> <dd>

17

Privilège non détenu.

</dd> <dt>


</dt> <dd>

21

Paramètre non valide.

</dd> </dl>

## <a name="remarks"></a>Notes

Actuellement, cette méthode n’est pas implémentée par WMI. Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="examples"></a>Exemples

l’Visual Basic code de Script suivant appelle la méthode **TakeOwnerShipEx** pour prendre possession du dossier C : \\ temp.


```VB
strComputer = "." 
Set objWMIService = GetObject( _
    "winmgmts:\\" & strComputer & "\root\CIMV2") 
' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")
' Obtain an InParameters object specific
' to the method.
Set objInParam = objShare.Methods_("TakeOwnerShipEx"). _
    inParameters.SpawnInstance_()

' Add the input parameters.
objInParam.Properties_.Item("Recursive") =  true

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod( _
    "Win32_Directory.Name='C:\Temp'", "TakeOwnerShipEx", objInParam)
wscript.echo objOutParams.ReturnValue
```



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

[\_Répertoire CIM](takeownershipex-method-in-class-cim-directory.md)
</dt> <dt>

[**\_Répertoire CIM**](cim-directory.md)
</dt> </dl>

 

