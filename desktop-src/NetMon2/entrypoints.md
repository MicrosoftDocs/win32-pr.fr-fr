---
description: La structure ENTRYPOINTS définit les points d’entrée pour les fonctions d’exportation que Moniteur réseau utilise pour exécuter l’analyseur.
ms.assetid: e2ac118d-e04b-489f-877f-84cc9888f8af
title: ENTRYPOINTS, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ENTRYPOINTS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3eebee878cd907ee20674224a969c82038f4ac6b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229649"
---
# <a name="entrypoints-structure"></a>ENTRYPOINTS, structure

La structure **ENTRYPOINTS** définit les points d’entrée pour les fonctions d’exportation que Moniteur réseau utilise pour exécuter l’analyseur.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct __ENTRYPOINTS {
  REGISTER         Register;
  DEREGISTER       Deregister;
  RECOGNIZEFRAME   RecognizeFrame;
  ATTACHPROPERTIES AttachProperties;
  FORMATPROPERTIES FormatProperties;
} ENTRYPOINTS, *LPENTRYPOINTS;
```



## <a name="members"></a>Membres

<dl> <dt>

**S’inscrire**
</dt> <dd>

Pointeur vers l’implémentation de la fonction d' [*expert d’inscription*](register-expert.md) .

</dd> <dt>

**Désinscrire**
</dt> <dd>

Pointeur vers l’implémentation de la fonction de [**désinscription**](deregister.md) .

</dd> <dt>

**RecognizeFrame**
</dt> <dd>

Pointeur vers l’implémentation de la fonction d’exportation [**RecognizeFrame**](recognizeframe.md) .

</dd> <dt>

**AttachProperties**
</dt> <dd>

Pointeur vers l’implémentation de la fonction d’exportation [**AttachProperties**](attachproperties.md) .

</dd> <dt>

**FormatProperties**
</dt> <dd>

Pointeur vers l’implémentation de la fonction d’exportation [**FormatProperties**](formatproperties.md) .

</dd> </dl>

## <a name="remarks"></a>Notes

La fonction **CreateProtocol** utilise la structure **ENTRYPOINTS** pour fournir des pointeurs vers Moniteur réseau. Les pointeurs doivent être spécifiés dans l’ordre identifié dans la section membres précédents.

La fonction [**FormatProperties**](formatproperties.md) n’a pas besoin d’être implémentée si Moniteur réseau n’affichera jamais les données de protocole. Par exemple, **FormatProperties** n’a pas besoin d’être implémenté si une application d’exportation utilise la sortie de l’analyseur, et moniteur réseau n’affiche pas la sortie.



| Pour plus d’informations sur                                        | Consultez                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| Ce que sont les analyseurs et comment ils fonctionnent avec Moniteur réseau. | [Analyseurs](parsers.md)                                  |
| L’implémentation de **DllMain**  comprend un exemple.        | [Implémentation de DllMain](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[AttachProperties](attachproperties.md)
</dt> <dt>

[CreateProtocol](createprotocol.md)
</dt> <dt>

[Désinscrire](deregister.md)
</dt> <dt>

[FormatProperties](formatproperties.md)
</dt> <dt>

[RecognizeFrame](recognizeframe.md)
</dt> <dt>

[S’inscrire](register-parser.md)
</dt> </dl>

 

 




