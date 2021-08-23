---
description: Définit les données à utiliser dans la vérification Microsoft Authenticode des données d’élément.
ms.assetid: 73c0e84f-7d59-4efa-927d-af8d7305bc9d
title: Structure PST_AUTHENTICODEDATA (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_AUTHENTICODEDATA
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: abf5bc69fd36e45cc715b3805f5407e821cfc7efc7f6595bcfc9eab8d762b716
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690859"
---
# <a name="pst_authenticodedata-structure"></a>AUTHENTICODEDATA PST ( \_ structure)

\[le Stockage protégé (Pstore) peut être utilisé dans Windows Server 2003 et Windows XP. elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Définit les données à utiliser dans la vérification Microsoft Authenticode des données d’élément.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD    cbSize;
  DWORD    dwModifiers;
  LPCWSTR  szRootCA;
  LPCWSTR  szIssuer;
  LPCWSTR  szPublisher;
  LPCWSTR  szProgramName;
} PST_AUTHENTICODEDATA, *PPST_AUTHENTICODE_DATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**cbSize**
</dt> <dd>

La taille de cette structure.

</dd> <dt>

**dwModifiers**
</dt> <dd>

Valeur qui identifie le modificateur que l’une des chaînes d’appelants doit vérifier.



| Valeur                                                                                                                                                                                                                                                 | Signification                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_AC_SINGLE_CALLER"></span><span id="pst_ac_single_caller"></span><dl> <dt>**Fichier PST \_ \_ \_ Appelant unique AC**</dt> <dt>0</dt> </dl>           | Un seul niveau dans la chaîne d’appel à PStore. L’appelant passe le contrôle de vérification. L’image spécifiée est l’appelant immédiat et est une application (.exe).<br/>              |
| <span id="PST_AC_TOP_LEVEL_CALLER"></span><span id="pst_ac_top_level_caller"></span><dl> <dt>**Fichier PST \_ \_Appelant de \_ niveau \_ supérieur AC**</dt> <dt>1</dt> </dl> | L’appelant de niveau supérieur doit réussir la vérification, mais il peut y avoir des dll intermédiaires. L’image spécifiée n’est pas nécessairement l’appelant immédiat et est une application (.exe).<br/>           |
| <span id="PST_AC_IMMEDIATE_CALLER"></span><span id="pst_ac_immediate_caller"></span><dl> <dt>**Fichier PST \_ \_ \_ Appelant immédiat AC**</dt> <dt>2</dt> </dl>  | L’appelant immédiat doit réussir la vérification, mais ne doit pas nécessairement être le processus de niveau supérieur. L’image spécifiée est l’appelant immédiat, et l’image peut être une application (.exe) ou une DLL.<br/> |



 

</dd> <dt>

**szRootCA**
</dt> <dd>

Pointeur vers une chaîne de caractères larges qui représente l’autorité de certification racine pour le certificat ; Utilisez la **valeur null** pour utiliser une autorité de certification disponible.

</dd> <dt>

**szIssuer**
</dt> <dd>

Pointeur vers une chaîne de caractères larges qui représente l’autorité de certification qui a émis le certificat ; Utilisez la **valeur null** pour utiliser une autorité de certification disponible.

</dd> <dt>

**szPublisher**
</dt> <dd>

Pointeur vers une chaîne de caractères larges qui représente l’éditeur de logiciel ; Utilisez la **valeur null** pour utiliser une autorité de certification disponible.

</dd> <dt>

**szProgramName**
</dt> <dd>

Pointeur vers une chaîne de caractères larges qui représente le nom du programme ; Utilisez la **valeur null** pour utiliser une autorité de certification disponible.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Pstore. h</dt> </dl> |



 

 
