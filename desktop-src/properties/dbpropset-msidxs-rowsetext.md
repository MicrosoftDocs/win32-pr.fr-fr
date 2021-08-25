---
description: Étend les propriétés définies pour les API d’ensemble de lignes.
ms.assetid: C1A2DF19-C68D-42CC-9CB2-190F22CB4158
title: DBPROPSET_MSIDXS_ROWSETEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f8c647d4b1ecbf9e5cc88ccae4af649c27093472456377e478ff80f7a76f3a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776409"
---
# <a name="dbpropset_msidxs_rowsetext"></a>DBPROPSET \_ MSIDXS \_ ROWSETEXT

Étend les propriétés définies pour les API d’ensemble de lignes.

``` syntax
#define DBPROPSET_MSIDXS_ROWSETEXT \
    { 0xaa6ee6b0, 0xe828, 0x11d0, \
        { 0xb2, 0x3e, 0x00, 0xaa, 0x00, 0x47, 0xfc, 0x01 } }
```

Le \_ jeu de \_ Propriétés ROWSETEXT DBPROPSET MSIDXS contient les constantes de propriété suivantes :

<dl> <dt>

<span id="MSIDXSPROP_ROWSETQUERYSTATUS"></span><span id="msidxsprop_rowsetquerystatus"></span>MSIDXSPROP \_ ROWSETQUERYSTATUS
</dt> <dd>

ID de propriété 2. État de la requête pour l’ensemble de lignes. Les \_ \* constantes stat indiquent l’état d’exécution et de fiabilité.

</dd> <dt>

<span id="MSIDXSPROP_COMMAND_LOCALE_STRING"></span><span id="msidxsprop_command_locale_string"></span>\_chaîne de \_ paramètres régionaux de commande MSIDXSPROP \_
</dt> <dd>

ID de propriété 3. Chaîne de paramètres régionaux qui représente la langue et les paramètres régionaux à utiliser pour cet ensemble de lignes.

</dd> <dt>

<span id="MSIDXSPROP_QUERY_RESTRICTION"></span><span id="msidxsprop_query_restriction"></span>\_restriction de requête MSIDXSPROP \_
</dt> <dd>

ID de propriété 4. Chaîne de requête associée à cet ensemble de lignes.

</dd> <dt>

<span id="MSIDXSPROP_PARSE_TREE"></span><span id="msidxsprop_parse_tree"></span>\_arborescence d’analyse MSIDXSPROP \_
</dt> <dd>

ID de propriété 5.

</dd> <dt>

<span id="MSIDXSPROP_MAX_RANK___"></span><span id="msidxsprop_max_rank___"></span>\_classement Max \_ MSIDXSPROP 
</dt> <dd>

ID de propriété 6.

</dd> <dt>

<span id="MSIDXSPROP_RESULTS_FOUND"></span><span id="msidxsprop_results_found"></span>résultats de MSIDXSPROP \_ \_ trouvés
</dt> <dd>

ID de propriété 7.

</dd> <dt>

<span id="MSIDXSPROP_WHEREID"></span><span id="msidxsprop_whereid"></span>MSIDXSPROP \_ WHEREID
</dt> <dd>

ID de propriété 8.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_VERSION_"></span><span id="msidxsprop_server_version_"></span>\_version du serveur MSIDXSPROP \_ 
</dt> <dd>

nouveauté de Windows 7. ID de propriété 9. Version du serveur.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_WINVER_MAJOR"></span><span id="msidxsprop_server_winver_major"></span>MSIDXSPROP \_ Server \_ winver \_ major
</dt> <dd>

ID de propriété 10.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_WINVER_MINOR"></span><span id="msidxsprop_server_winver_minor"></span>\_serveur MSIDXSPROP \_ - \_ mineur mineur
</dt> <dd>

ID de propriété 11.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_NLSVERSION"></span><span id="msidxsprop_server_nlsversion"></span>\_serveur MSIDXSPROP \_ NLSVERSION
</dt> <dd>

ID de propriété 12.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_NLSVER_DEFINED_"></span><span id="msidxsprop_server_nlsver_defined_"></span>MSIDXSPROP \_ Server \_ NLSVER \_ défini 
</dt> <dd>

ID de propriété 13.

</dd> <dt>

<span id="MSIDXSPROP_SAME_SORTORDER_USED_"></span><span id="msidxsprop_same_sortorder_used_"></span>MSIDXSPROP \_ même \_ SORTORDER \_ utilisé 
</dt> <dd>

ID de propriété 14.

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour interroger \_ \_ la version du serveur MSIDXSPROP, il est nécessaire d’émettre la requête factice sur le serveur, comme dans l’exemple suivant.

`SELECT top 1 workid from servername.systemindex`

Une fois l’ensemble de lignes retourné, appelez [**IUnknown :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour les fonctionnalités de l’ensemble de lignes, puis appelez [IRowsetInfo :: GetProperties](/previous-versions/windows/desktop/ms719611(v=vs.85)) pour la nouvelle propriété (MSIDXSPROP \_ Server \_ version). La propriété a un type **VT \_ I4** et peut prendre l’une des valeurs suivantes :

\#définir la version de l’élément de configuration \_ \_ WDS30 0x102//258

\#définir la version de l’élément de configuration \_ \_ WDS40 0x109//265

\#définir la version de l’élément de configuration \_ \_ WIN70 0X700//1792

Une fois que la valeur est connue, le client peut former une requête prise en charge par le serveur et émettre une requête réelle.

DBPROPSET \_ MSIDXS \_ ROWSETEXT est déclaré dans NTQuery. h.

 

 
