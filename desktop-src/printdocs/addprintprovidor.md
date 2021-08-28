---
description: La fonction AddPrintProvidor installe un fournisseur d’impression local et lie les fichiers de configuration, de données et de fournisseur.
ms.assetid: f34549c3-0474-48ba-9307-5b36f02dbe1c
title: AddPrintProvidor, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrintProvidor
- AddPrintProvidorA
- AddPrintProvidorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: c5738f2a9dbf7da4a2dcddb952891b415af73cb7
ms.sourcegitcommit: 58ca2495eae63806264bf4594db45aae692c70b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "122021693"
---
# <a name="addprintprovidor-function"></a>AddPrintProvidor fonction)

> [!IMPORTANT]
> Le 6 juillet 2021, [KB5005010](https://support.microsoft.com/topic/kb5005010-restricting-installation-of-new-printer-drivers-after-applying-the-july-6-2021-updates-31b91c02-05bc-4ada-a7ea-183b129578a7) a introduit une option de configuration basée sur le Registre facultative pour restreindre l’accès à cette API uniquement aux utilisateurs administrateurs. Cette option était désactivée par défaut.
>
> Le 10 août 2021, [KB5005652](https://aka.ms/print_install_kb) modifie la valeur par défaut de cette configuration pour exiger des droits d’administrateur pour installer de nouveaux pilotes d’imprimante.

La fonction **AddPrintProvidor** installe un fournisseur d’impression local et lie les fichiers de configuration, de données et de fournisseur.

## <a name="syntax"></a>Syntaxe


```C++
BOOL AddPrintProvidor(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pProviderInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur sur lequel le fournisseur doit être installé. Pour les systèmes qui prennent uniquement en charge l’installation locale de fournisseurs, ce paramètre doit avoir la **valeur null**.

</dd> <dt>

De *niveau* \[ dans\]
</dt> <dd>

Niveau de la structure vers laquelle *pProviderInfo* pointe. Il peut s’agir de l’une des valeurs suivantes.



| Valeur                                                                                                | Signification                                                                            |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | La fonction utilise une structure [**PROVIDOR \_ info \_ 1**](providor-info-1.md) .<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | La fonction utilise une structure [**PROVIDOR \_ info \_ 2**](providor-info-2.md) .<br/> |



 

</dd> <dt>

*pProviderInfo* \[ dans\]
</dt> <dd>

Pointeur vers une structure de fournisseur d’impression, comme indiqué par *Level*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Remarques

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

Avant qu’une application appelle la fonction **AddPrintProvidor** , tous les fichiers requis par le fournisseur doivent être copiés dans le répertoire system32.

Un fournisseur ajouté par **AddPrintProvidor** peut être supprimé en appelant [**DeletePrintProvidor**](deleteprintprovidor.md).

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **AddPrintProvidorW** (Unicode) et **AddPrintProvidorA** (ANSI)<br/>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrintProvidor**](deleteprintprovidor.md)
</dt> <dt>

[**\_Informations PROVIDOR \_ 1**](providor-info-1.md)
</dt> <dt>

[**\_Informations PROVIDOR \_ 2**](providor-info-2.md)
</dt> </dl>

 

 




