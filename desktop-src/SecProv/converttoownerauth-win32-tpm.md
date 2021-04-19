---
description: Traduit une entrée de phrase secrète fournie par l’utilisateur en une autorisation de propriétaire de 20 octets qui peut être utilisée pour interagir avec le module de plateforme sécurisée. Les méthodes telles que TakeOwnership et ResetAuthLockOut requièrent la valeur d’autorisation du propriétaire qui en résulte.
ms.assetid: 69eed934-1668-495a-b5b7-cd4a87df1ab3
title: Méthode ConvertToOwnerAuth de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ConvertToOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: f3de5803d10458156fb453e964d782f7c9760333
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536738"
---
# <a name="converttoownerauth-method-of-the-win32_tpm-class"></a>Méthode ConvertToOwnerAuth de la \_ classe TPM Win32

La méthode **ConvertToOwnerAuth** de la [**classe \_ TPM Win32**](win32-tpm.md) traduit une entrée de phrase secrète fournie par l’utilisateur en une autorisation de propriétaire de 20 octets qui peut être utilisée pour interagir avec le module de plateforme sécurisée. Les méthodes telles que [**TakeOwnership**](takeownership-win32-tpm.md) et [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) requièrent la valeur d’autorisation du propriétaire qui en résulte.

Le processus de conversion suit les spécifications de la [Trusted Computing Group](https://www.trustedcomputinggroup.org/).

## <a name="syntax"></a>Syntaxe


```mof
uint32 ConvertToOwnerAuth(
  [in]  string OwnerPassPhrase,
  [out] string OwnerAuth
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*OwnerPassPhrase* \[ dans\]
</dt> <dd>

Type : **chaîne**

Chaîne à convertir en valeur d’autorisation du propriétaire. La chaîne peut contenir un nombre quelconque de caractères alphanumériques.

</dd> <dt>

*Origine* \[ à\]
</dt> <dd>

Type : **chaîne**

Chaîne dérivée du paramètre *OwnerPassPhrase* . Cette valeur est une valeur binaire de 20 octets encodée en une chaîne de 28 octets se terminant par un caractère **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.

Les tableaux suivants répertorient certains des codes de retour courants.



| Code/valeur de retour                                                                                                                                 | Description                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | La méthode a réussi.<br/> |



 

## <a name="remarks"></a>Notes

Une chaîne encodée UTF-16LE Unicode est convertie en valeur d’autorisation du propriétaire du module de plateforme sécurisée (TPM) de 20 octets en acceptant le hachage SHA-1 de la représentation binaire de la chaîne. La fin **null** de la chaîne Unicode n’est pas incluse dans le hachage. Aucun Salt n’est utilisé dans le hachage SHA-1.

Par exemple, pour convertir la phrase secrète du propriétaire du module de plateforme sécurisée « 1Sample » en valeur d’autorisation du propriétaire du module de plateforme sécurisée, le hachage SHA-1 est extrait du flux d’octets suivant :

`0x31 0x00 0x53 0x00 0x61 0x00 0x6D 0x00 0x70 0x00 0x6C 0x00 0x65 0x00`

Pour convertir une phrase secrète de longueur nulle en valeur d’autorisation du propriétaire, le hachage SHA-1 est pris dans le flux d’octets **null** .

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                      |
| Espace de noms<br/>                | Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>\_TPM. mof Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TPM Win32**](win32-tpm.md)
</dt> <dt>

[**TakeOwnership**](takeownership-win32-tpm.md)
</dt> </dl>

 

 
