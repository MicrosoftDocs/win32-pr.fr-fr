---
description: Fournit des informations aux méthodes de l’interface IQueryAssociations.
ms.assetid: e67d0282-9090-43e6-aedf-bb1fc0443221
title: Énumération ASSOCF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b92a917baf518d8b6f1ebba196e6c3e53e9fdb9
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520284"
---
# <a name="assocf-enumeration"></a>Énumération ASSOCF

Fournit des informations aux méthodes de l’interface [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) .

## <a name="syntax"></a>Syntax

```cpp
typedef enum  {
    ASSOCF_NONE                  = 0x00000000,  
    ASSOCF_INIT_NOREMAPCLSID     = 0x00000001,  
    ASSOCF_INIT_BYEXENAME        = 0x00000002,  
    ASSOCF_OPEN_BYEXENAME        = 0x00000002,  
    ASSOCF_INIT_DEFAULTTOSTAR    = 0x00000004,  
    ASSOCF_INIT_DEFAULTTOFOLDER  = 0x00000008,  
    ASSOCF_NOUSERSETTINGS        = 0x00000010,  
    ASSOCF_NOTRUNCATE            = 0x00000020,  
    ASSOCF_VERIFY                = 0x00000040,  
    ASSOCF_REMAPRUNDLL           = 0x00000080,  
    ASSOCF_NOFIXUPS              = 0x00000100,  
    ASSOCF_IGNOREBASECLASS       = 0x00000200,  
    ASSOCF_INIT_IGNOREUNKNOWN    = 0x00000400,  
    ASSOCF_INIT_FIXED_PROGID     = 0x00000800,  
    ASSOCF_IS_PROTOCOL           = 0x00001000,  
    ASSOCF_INIT_FOR_FILE         = 0x00002000
} ASSOCF;
```

## <a name="constants"></a>Constantes

 <span id="ASSOCF_NONE"></span><span id="assocf_none"></span>**ASSOCF \_ aucun** 

Aucune des options suivantes n’est définie.

 <span id="ASSOCF_INIT_NOREMAPCLSID"></span><span id="assocf_init_noremapclsid"></span>**ASSOCF \_ init \_ NOREMAPCLSID** 

Ordonne aux méthodes de l’interface [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) de ne pas mapper les valeurs CLSID aux valeurs ProgID.

 <span id="ASSOCF_INIT_BYEXENAME"></span><span id="assocf_init_byexename"></span>**ASSOCF \_ init \_ BYEXENAME** 

Identifie la valeur du paramètre *pwszAssoc* de [**IQueryAssociations :: init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init) comme un nom de fichier exécutable. Si cet indicateur n’est pas défini, la clé racine est définie sur le ProgID associé à la clé de **.exe** au lieu du ProgID du fichier exécutable.

 <span id="ASSOCF_OPEN_BYEXENAME"></span><span id="assocf_open_byexename"></span>**ASSOCF \_ ouvrir \_ BYEXENAME** 

Identique à **ASSOCF \_ init \_ BYEXENAME**.

 <span id="ASSOCF_INIT_DEFAULTTOSTAR"></span><span id="assocf_init_defaulttostar"></span>**ASSOCF \_ init \_ DEFAULTTOSTAR** 

Spécifie que lorsqu’une méthode [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) ne trouve pas la valeur demandée sous la clé racine, elle doit tenter de récupérer la valeur comparable de la **\*** sous-clé.

 <span id="ASSOCF_INIT_DEFAULTTOFOLDER"></span><span id="assocf_init_defaulttofolder"></span>**ASSOCF \_ init \_ DEFAULTTOFOLDER** 

Spécifie que lorsqu’une méthode [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) ne trouve pas la valeur demandée sous la clé racine, elle doit tenter de récupérer la valeur comparable de la sous-clé de **dossier** .

 <span id="ASSOCF_NOUSERSETTINGS"></span><span id="assocf_nousersettings"></span>**ASSOCF \_ NOUSERSETTINGS** 

Spécifie que seules les **\_ classes HKEY \_** doivent être recherchées et que **HKEY \_ Current \_ User** doit être ignoré.

 <span id="ASSOCF_NOTRUNCATE"></span><span id="assocf_notruncate"></span>**ASSOCF \_ NOTRUNCATE** 

Spécifie que la chaîne de retour ne doit pas être tronquée. Au lieu de cela, retournez une valeur d’erreur et la taille requise pour la chaîne complète.

 <span id="ASSOCF_VERIFY"></span><span id="assocf_verify"></span>**ASSOCF \_ vérifier** 

Ordonne aux méthodes [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) de vérifier que les données sont exactes. Ce paramètre permet aux méthodes **IQueryAssociations** de lire des données à partir du disque dur de l’utilisateur à des fins de vérification. Par exemple, ils peuvent vérifier le nom convivial dans le registre par rapport à celui stocké dans le fichier .exe. La définition de cet indicateur réduit généralement l’efficacité de la méthode.

 <span id="ASSOCF_REMAPRUNDLL"></span><span id="assocf_remaprundll"></span>**ASSOCF \_ REMAPRUNDLL** 

Fait en sorte que les méthodes [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) ignorent Rundll.exe et retournent des informations sur sa cible. En général, les méthodes **IQueryAssociations** retournent des informations sur la première .exe ou .dll dans une chaîne de commande. Si une commande utilise Rundll.exe, la définition de cet indicateur indique à la méthode d’ignorer Rundll.exe et de retourner des informations sur sa cible.

 <span id="ASSOCF_NOFIXUPS"></span><span id="assocf_nofixups"></span>**ASSOCF \_ NOFIXUPS** 

Ordonne aux méthodes [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) de ne pas corriger les erreurs dans le registre, telles que le nom convivial d’une fonction qui ne correspond pas à celui trouvé dans le fichier .exe.

 <span id="ASSOCF_IGNOREBASECLASS"></span><span id="assocf_ignorebaseclass"></span>**ASSOCF \_ IGNOREBASECLASS** 

Spécifie que la valeur de BaseClass doit être ignorée.

 <span id="ASSOCF_INIT_IGNOREUNKNOWN"></span><span id="assocf_init_ignoreunknown"></span>**ASSOCF \_ init \_ IGNOREUNKNOWN** 

**introduite dans Windows 7**. Spécifie que le ProgID « inconnu » doit être ignoré ; au lieu de cela, échoue.

 <span id="ASSOCF_INIT_FIXED_PROGID"></span><span id="assocf_init_fixed_progid"></span>**ASSOCF \_ init \_ ( \_ ProgID fixe)** 

**Introduite dans Windows 8**. Spécifie que le ProgID fourni doit être mappé à l’aide des valeurs par défaut du système, plutôt que les valeurs par défaut de l’utilisateur actuel.

 <span id="ASSOCF_IS_PROTOCOL"></span><span id="assocf_is_protocol"></span>**ASSOCF \_ est un \_ protocole** 

**Introduite dans Windows 8**. Spécifie que la valeur est un protocole et doit être mappée à l’aide des valeurs par défaut de l’utilisateur actuel.

 <span id="ASSOCF_INIT_FOR_FILE"></span><span id="assocf_init_for_file"></span>**ASSOCF \_ init \_ pour le \_ fichier** 

**Introduite dans Windows 8.1**. Spécifie que le ProgID correspond à une association basée sur une extension de fichier. À utiliser avec **ASSOCF \_ init \_ \_ identificateur programmatique fixe**.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]               |
| Serveur minimal pris en charge | Windows 2000 Server - \[Applications de bureau uniquement\]                                 |
| En-tête                   |  Shlwapi. h  |



## <a name="see-also"></a>Voir aussi

 [**AssocQueryKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerykeya) [**AssocQueryString**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) [**AssocQueryStringByKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) 

 

 

© 2017 Microsoft. Tous droits réservés.
