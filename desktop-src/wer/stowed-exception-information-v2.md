---
title: Structure STOWED_EXCEPTION_INFORMATION_V2
description: Contient les informations sur les exceptions arrimées.
ms.assetid: 79267974-EE1B-4427-A6D6-265F6BC5D73A
keywords:
- STOWED_EXCEPTION_INFORMATION_V2 structure Rapport d’erreurs Windows
- pointeur de structure PSTOWED_EXCEPTION_INFORMATION_V2 Rapport d’erreurs Windows
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_V2
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefd313f0edcc122708f141cd65418beaade03a9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294487"
---
# <a name="stowed_exception_information_v2-structure"></a>Structure d' \_ informations d’exception de la \_ \_ version v2

Contient les informations sur les exceptions arrimées.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_V2 {
  STOWED_EXCEPTION_INFORMATION_HEADER Header;
  HRESULT                             ResultCode;
  struct {
    DWORD ExceptionForm  :2;
    DWORD ThreadId  :30;
  };
  union {
    struct {
      PVOID ExceptionAddress;
      ULONG StackTraceWordSize;
      ULONG StackTraceWords;
      PVOID StackTrace;
    };
    struct {
      PWSTR ErrorText;
    };
  };
  ULONG                               NestedExceptionType;
  PVOID                               NestedException;
} STOWED_EXCEPTION_INFORMATION_V2, *PSTOWED_EXCEPTION_INFORMATION_V2;
```



## <a name="members"></a>Membres

<dl> <dt>

**En-tête**
</dt> <dd>

Type : **[ **\_ \_ \_ en-tête d’informations d’exception arrimé**](stowed-exception-information-header.md)**

</dd> <dd>

Structure d' [**\_ \_ \_ en-tête d’informations d’exception arrimé**](stowed-exception-information-header.md) qui contient des informations pour cette structure parente.

</dd> <dt>

**ResultCode**
</dt> <dd>

Type : **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Code [**HRESULT**](/windows/desktop/WinProg/windows-data-types) de l’exception arrimée.

</dd> <dt>

**ExceptionForm**
</dt> <dd>

Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valeur 2 bits qui identifie le formulaire de l’exception.



| Valeur                                                                                                                                                                                                                                                                  | Signification                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_FORM_BINARY"></span><span id="stowed_exception_form_binary"></span><dl> <dt>**Rangé \_ \_ \_ Binaire de formulaire d’exception**</dt> <dt>0x01</dt> </dl> | Cette valeur indique que la forme de l’exception est binaire.<br/> |
| <span id="STOWED_EXCEPTION_FORM_TEXT"></span><span id="stowed_exception_form_text"></span><dl> <dt>**Rangé \_ \_ \_ Texte de formulaire d’exception**</dt> <dt>0x02</dt> </dl>       | Cette valeur indique que le formulaire de l’exception est du texte.<br/>   |



 

</dd> <dt>

**ThreadId**
</dt> <dd>

Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valeur de 30 bits qui identifie le thread qui a levé l’exception. La valeur est décalée vers la droite de 2 bits lorsqu’elle est stockée. Pour le reconvertir en un ID de thread valide, décalez la valeur vers la gauche de 2. Par exemple :

``` syntax
DWORD ActualThreadId = (StowedException.ThreadId << 2);
```

</dd> <dt>

(*struct sans nom*)
</dt> <dd>

Les membres de cette structure imbriquée ne sont valides que si le membre **ExceptionForm** est défini sur le type d' **\_ exception \_ \_ arrimé**.

<dl> <dt>

**ExceptionAddress**
</dt> <dd>

Type : **[ **pVoid**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Pointeur qui contient l’adresse de l’exception.

</dd> <dt>

**StackTraceWordSize**
</dt> <dd>

Type : **[ **ULong**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Taille, en octets, de chaque mot de la trace de la pile vers lequel pointe le membre **StackTrace** . Cette valeur est définie sur 4 pour les plateformes 32 bits et 8 pour les plateformes 64 bits.

</dd> <dt>

**StackTraceWords**
</dt> <dd>

Type : **[ **ULong**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre de mots dans la trace de la pile vers lequel pointe le membre **StackTrace** . Le nombre de mots est égal au nombre d’éléments dans le tableau.

</dd> <dt>

**Trace**
</dt> <dd>

Type : **[ **pVoid**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Pointeur vers un bloc de mémoire qui contient la trace de la pile.

</dd> </dl> </dd> <dt>

(*struct sans nom*)
</dt> <dd>

Le membre de cette structure imbriquée est valide uniquement si le membre **ExceptionForm** est défini sur le **\_ \_ \_ texte de formulaire d’exception arrimé**.

<dl> <dt>

**ErrorText**
</dt> <dd>

Type : **[ **PWSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui contient le texte d’erreur de l’exception.

</dd> </dl> </dd> <dt>

**NestedExceptionType**
</dt> <dd>

Type : **[ **ULong**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valeur 32 bits qui spécifie le type d’objet vers lequel pointe le membre **NestedException** . Définissez la valeur avec cette macro de définition de type d’échange d’octets qui suppose un faible endian :

``` syntax
#define STOWED_EXCEPTION_NESTED_TYPE(t) ((((((ULONG)(t)) >> 24) & 0xFF) <<  0) | \
                                         (((((ULONG)(t)) >> 16) & 0xFF) <<  8) | \
                                         (((((ULONG)(t)) >>  8) & 0xFF) << 16) | \
                                         (((((ULONG)(t)) >>  0) & 0xFF) << 24))
```

Voici quelques définitions de type courantes :



| Valeur                                                                                                                                                                                                                                                                                                                           | Signification                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_NESTED_TYPE_NONE"></span><span id="stowed_exception_nested_type_none"></span><dl> <dt>**Rangé \_ \_Type imbriqué d' \_ exception \_ None**</dt> <dt>(0x00000000)</dt> </dl>                                  | Cette valeur spécifie qu’il n’existe aucun objet exception imbriqué.<br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_WIN32"></span><span id="stowed_exception_nested_type_win32"></span><dl> <dt>**Rangé \_ \_Type imbriqué d' \_ exception \_**</dt> type imbriqué <dt> \_ de l’exception Win32 \_ \_ ('W32E')</dt> </dl>    | Cette valeur spécifie que le membre **NestedException** pointe vers un objet [**\_ enregistrement d’exception**](/windows/desktop/api/winnt/ns-winnt-exception_record) .<br/>                                                                                                                                                                                                                                                              |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_STOWED"></span><span id="stowed_exception_nested_type_stowed"></span><dl> <dt>**Rangé \_ exception \_ \_ \_**</dt> type imbriqué <dt>de l’exception arrimé de type imbriqué \_ \_ \_ ('arrim')</dt> </dl> | Cette valeur spécifie que le membre **NestedException** pointe vers un autre objet exception rangé. L’autre objet d’exception arrimée peut être un objet d’informations d’exception chargées **\_ \_ \_ v2** ou une version différente avec un membre d' **en-tête** valide, autrement dit un membre d' **en-tête** qui contient un [**\_ \_ \_ en-tête d’informations d’exception arrimé**](stowed-exception-information-header.md)valide.<br/> |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_CLR"></span><span id="stowed_exception_nested_type_clr"></span><dl> <dt>**Rangé \_ Type imbriqué d’EXCEPTION type imbriqué de l’exception \_ \_ \_ CLR**</dt> <dt> \_ \_ \_ ('CLR1 ')</dt> </dl>          | Cette valeur spécifie que le membre **NestedException** pointe vers un objet d’exception « CLR1 ».<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_LEO"></span><span id="stowed_exception_nested_type_leo"></span><dl> <dt>**Rangé \_ \_Type imbriqué d' \_ exception \_**</dt> type imbriqué <dt> \_ de l’exception Leo \_ \_ ('LEO1 ')</dt> </dl>          | Cette valeur spécifie que le membre **NestedException** pointe vers un objet d’exception de langage.<br/>                                                                                                                                                                                                                                                                                               |



 

</dd> <dt>

**NestedException**
</dt> <dd>

Type : **[ **pVoid**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Pointeur vers un type d’exception imbriquée. Le type d’objet est indiqué par le membre **NestedExceptionType** .

</dd> </dl>

## <a name="remarks"></a>Notes

**Rangé \_ Les \_ informations \_ sur l’exception v2** et l' [**\_ \_ \_ en-tête d’informations d’exception arrimées**](stowed-exception-information-header.md) ne sont actuellement pas définis dans un en-tête disponible publiquement. vous devez donc les définir dans votre code source avant de les utiliser.

La structure d’informations d’exception de la version **\_ \_ \_ v1** est identique à cette structure, sauf qu’elle ne contient pas les membres **NestedExceptionType** et **NestedException** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                         |
| En-tête<br/>                   | <dl> <dt>Aucun</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**enregistrement d’EXCEPTION \_**](/windows/desktop/api/winnt/ns-winnt-exception_record)
</dt> <dt>

[**\_ \_ en-tête d’informations d’exception arrimé \_**](stowed-exception-information-header.md)
</dt> </dl>

 

