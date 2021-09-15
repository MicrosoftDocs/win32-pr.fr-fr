---
description: Contient les attributs de partage DDE gérés par le gestionnaire de base de données du partage NetDDE (DSDM).
ms.assetid: f4101553-06ef-4f83-87c7-5b6fdf0467e5
title: NDDESHAREINFO, structure (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDDESHAREINFO
api_type:
- HeaderDef
api_location:
- Nddeapi.h
ms.openlocfilehash: 975382272a4e2c7cc56b0ddf593905b4d745a48b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403911"
---
# <a name="nddeshareinfo-structure"></a>NDDESHAREINFO, structure

\[Le DDE réseau n’est plus pris en charge. Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]

Contient les attributs de partage DDE gérés par le gestionnaire de base de données du partage NetDDE (DSDM). Le descripteur de sécurité associé à chaque partage DDE n’est pas transmis via cette structure, mais est accessible via des fonctions spécifiques. L’API DSDM NetDDE accepte cette structure pour les fonctions set. pour les fonctions d’extraction, le DSDM retourne la structure compressée dans la mémoire tampon fournie avec les données référencées par les membres **lpszShareName**, **lpszAppTopicList** et **lpszItemList**.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _NDDESHAREINFO {
  LONG   lRevision;
  LPTSTR lpszShareName;
  LONG   lShareType;
  LPTSTR lpszAppTopicList;
  LONG   fSharedFlag;
  LONG   fService;
  LONG   fStartAppFlag;
  LONG   nCmdShow;
  LONG   qModifyId[2];
  LONG   cNumItems;
  LPTSTR lpszItemList;
} NDDESHAREINFO, *PNDDESHAREINFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**lRevision**
</dt> <dd>

Niveau de révision de la structure **NDDESHAREINFO** . Actuellement, le niveau de révision est 1.

</dd> <dt>

**lpszShareName**
</dt> <dd>

Nom du partage. Cette chaîne ne doit pas être supérieure à la longueur maximale de \_ NDDESHARENAME caractères.

</dd> <dt>

**lShareType**
</dt> <dd>

Un ou plusieurs types de partage DDE. Ce membre peut être une combinaison des types de partage DDE pris en charge suivants.



| Type de partage                                                                                                                                                                                                                           | Signification                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SHARE_TYPE_NEW"></span><span id="share_type_new"></span><dl> <dt>**Partager \_ TAPEZ \_ New**</dt> <dt>0x02</dt> </dl>          | Le partage contient une paire application/rubrique OLE.<br/>   |
| <span id="SHARE_TYPE_OLD"></span><span id="share_type_old"></span><dl> <dt>**Partager \_ TAPEZ \_ Old**</dt> <dt>0x01</dt> </dl>          | Le partage contient une paire application/rubrique DDE.<br/>    |
| <span id="SHARE_TYPE_STATIC"></span><span id="share_type_static"></span><dl> <dt>**Partager \_ 0x04 \_ statique de type**</dt> <dt></dt> </dl> | Le partage contient une paire application/rubrique statique.<br/> |



 

</dd> <dt>

**lpszAppTopicList**
</dt> <dd>

Pointeur vers une mémoire tampon qui contient des chaînes se terminant par un caractère null pour les paires d’application/rubrique statiques DDE, OLE et. La mémoire tampon doit être au format suivant :

``` syntax
<DDE application name>|<DDE topic name>\0
<OLE application name>|<OLE topic name>\0
<static application name>|<static topic name>\0\0
```

</dd> <dt>

**fSharedFlag**
</dt> <dd>

Si ce membre a la **valeur false**, le partage DDE n’autorise pas les utilisateurs distants à communiquer via ce dernier à l’aide de DDE. Toutefois, les utilisateurs locaux peuvent toujours communiquer via le partage DDE. Les liens client locaux sont toujours implicites si le DACL associé accorde l’accès.

</dd> <dt>

**fService**
</dt> <dd>

Si ce membre est défini, le partage DDE ne vérifie pas si l’utilisateur actuel l’a défini comme approuvé avant d’autoriser la communication DDE.

</dd> <dt>

**fStartAppFlag**
</dt> <dd>

Si ce membre est défini et que le partage est approuvé pour démarrer des applications, NetDDE tente de démarrer l’application spécifiée par **lpszAppTopicList** s’il ne peut pas démarrer une conversation DDE avec l’application.

</dd> <dt>

**nCmdShow**
</dt> <dd>

Lorsque NetDDE démarre une application pour initier une conversation DDE, cette valeur est envoyée à l’application via le paramètre *nCmdShow* de la fonction [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) . Il définit le mode par défaut de la fenêtre d’application à afficher dans. Ce paramètre est significatif uniquement si **fStartAppFlag** est actif. L’utilisateur connecté dans le contexte duquel l’application est démarrée peut également remplacer cette option lors de la promotion de l’état de confiance du partage. La valeur par défaut de ce membre est SW \_ SHOWMAXIMIZED.

</dd> <dt>

**qModifyId**
</dt> <dd>

Numéro de série de 8 octets qui indique le numéro de série de modification du partage DDE. Chaque fois que le partage DDE est modifié par un appel [**NDdeShareSetInfo**](nddesharesetinfo.md) ou [**NDdeSetShareSecurity**](nddesetsharesecurity.md) , ces valeurs sont modifiées.

</dd> <dt>

**cNumItems**
</dt> <dd>

Nombre d’éléments figurant dans **lpszItemList**. Si **cNumItems** est égal à zéro, **lpszItemList** est vide, et les informations de partage et le descripteur de sécurité associé s’appliquent à tous les éléments qui ont été mis en service par l’application associée.

</dd> <dt>

**lpszItemList**
</dt> <dd>

Pointeur vers une mémoire tampon qui contient des chaînes se terminant par un caractère null qui spécifient les éléments que l’application cliente dans une transaction DDE peut demander ou pour démarrer des boucles de notification. Si aucun élément n’est répertorié, le partage DDE autorise l’utilisation de tout élément. Le nombre d’éléments dans la liste doit correspondre au nombre de **cNumItems** .

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[présentation du échange dynamique de données réseau](network-dynamic-data-exchange.md)
</dt> <dt>

[Structures DDE réseau](network-dde-structures.md)
</dt> <dt>

[**NDdeSetShareSecurity**](nddesetsharesecurity.md)
</dt> <dt>

[**NDdeShareSetInfo**](nddesharesetinfo.md)
</dt> <dt>

[**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain)
</dt> </dl>

 

