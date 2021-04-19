---
description: Écrit la ruche de Registre hors connexion spécifiée dans un fichier.
ms.assetid: 26f2eed9-e6e0-4dc0-8b91-212cde072744
title: ORSaveHive, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSaveHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 59df5b191a9bc0cfe98e1681665c5814935aa2c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539567"
---
# <a name="orsavehive-function"></a>ORSaveHive fonction)

Écrit la ruche de Registre hors connexion spécifiée dans un fichier.

## <a name="syntax"></a>Syntaxe


```C++
DWORD ORSaveHive(
  _In_ ORHKEY Handle,
  _In_ PCWSTR lpHivePath,
  _In_ DWORD  dwOsMajorVersion,
  _In_ DWORD  dwOsMinorVersion
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Gérer* \[ dans\]
</dt> <dd>

Handle de la ruche de Registre hors connexion à enregistrer.

</dd> <dt>

*lpHivePath* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne Unicode qui spécifie le nom du fichier ruche du Registre. Il ne peut pas s’agir du nom d’un fichier existant.

</dd> <dt>

*dwOsMajorVersion* \[ dans\]
</dt> <dd>

Numéro de version principale du système d’exploitation. Ce membre peut être l’une des valeurs suivantes.



| Valeur                                                                        | Signification                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>5</dt> </dl> | Si *dwOsMinorVersion* est 1, le système d’exploitation est Windows XP.<br/> Si *dwOsMinorVersion* est 2, le système d’exploitation est windows Server 2003 R2, windows Server 2003 ou Windows XP Professionnel Édition x64.<br/> |
| <dl> <dt>6</dt> </dl> | Si *dwOsMinorVersion* est égal à 0, le système d’exploitation est windows Server 2008 ou Windows Vista.<br/> Si *dwOsMinorVersion* est 1, le système d’exploitation est windows Server 2008 R2 ou Windows 7.<br/>                       |



 

</dd> <dt>

*dwOsMinorVersion* \[ dans\]
</dt> <dd>

Numéro de la version mineure du système d’exploitation. Ce membre peut être l’une des valeurs suivantes.



| Valeur                                                                        | Signification                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Si *dwOsMajorVersion* est 6, le système d’exploitation est windows Server 2008 ou Windows Vista.<br/>                                                                                                                                          |
| <dl> <dt>1</dt> </dl> | Si *dwOsMajorVersion* est 5, le système d’exploitation est Windows XP.<br/> Si *dwOsMajorVersion* est 6, le système d’exploitation est windows Server 2008 R2 ou Windows 7.<br/>                                                                |
| <dl> <dt>2</dt> </dl> | Si *dwOsMajorVersion* est 5, le système d’exploitation est windows Server 2003 R2, windows Server 2003 ou Windows XP Professionnel Édition x64. <br/> Si *dwOsMajorVersion* a la valeur 6, le paramètre *dwOsMinorVersion* doit avoir la valeur 0 ou 1. <br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h. Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur. Les codes d’erreur possibles sont les suivants :

-   Si l’appelant ne dispose pas des droits d’accès nécessaires pour écrire le fichier, la fonction retourne l’erreur \_ accès \_ refusé.
-   Si le fichier spécifié existe déjà, la fonction retourne l’erreur \_ déjà \_ existante.

## <a name="remarks"></a>Notes

La fonction **ORSaveHive** doit être utilisée pour enregistrer les modifications apportées à une ruche de Registre hors connexion. Les modifications ne sont pas conservées tant que **ORSaveHive** n’est pas appelé pour enregistrer la ruche dans un fichier.

Les paramètres *dwOsMajorVersion* et *dwOsMinorVersion* spécifient ensemble le format cible du fichier ruche du Registre. Le tableau suivant récapitule les numéros de version des systèmes d’exploitation les plus récents.



| Système d’exploitation                    | Numéro de version |
|-------------------------------------|----------------|
| Windows Server 2008 R2              | 6.1            |
| Windows 7                           | 6.1            |
| Windows Server 2008                 | 6.0            |
| Windows Vista                       | 6.0            |
| Windows Server 2003 R2              | 5.2            |
| Windows Server 2003                 | 5.2            |
| Windows XP Professionnel Édition x64 | 5.2            |
| Windows XP                          | 5,1            |



 

Utilisez la fonction [GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) pour récupérer des informations sur le système d’exploitation actuel.

La fonction **ORSaveHive** verrouille la ruche du Registre pendant qu’elle écrit la ruche dans le fichier, puis ferme le fichier et libère le verrou. La ruche du Registre reste en mémoire jusqu’à ce qu’elle soit fermée par l’appel de la fonction [**ORCloseHive**](orclosehive.md) . Il est possible d’apporter d’autres modifications à la ruche du Registre pendant qu’elle est ouverte ; Toutefois, pour conserver ces modifications, la ruche doit être enregistrée dans un nouveau fichier, car la fonction **ORSaveHive** ne remplacera pas un fichier existant.

La fonction **ORSaveHive** peut être utilisée pour enregistrer une partie de la ruche de Registre hors connexion. La clé spécifiée dans le paramètre *handle* devient la clé racine d’une ruche qui se compose de la clé spécifiée et de toutes ses sous-clés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|---------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | Bibliothèque du Registre hors connexion Windows version 1,0 ou ultérieure<br/>                      |
| En-tête<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Tourne](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> <dt>

[**ORCloseHive**](orclosehive.md)
</dt> <dt>

[**OROpenHive**](oropenhive.md)
</dt> </dl>

 

 
