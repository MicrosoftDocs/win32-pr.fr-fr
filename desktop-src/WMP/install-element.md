---
title: Élément d’installation
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. l’élément Install spécifie les valeurs utilisées par Lecteur Windows Media pour installer un magasin en ligne.
ms.assetid: 9a5e15ee-ec36-48d3-a1c2-bf20b6d2da48
keywords:
- Lecteur Windows Media d’élément d’installation
topic_type:
- apiref
api_name:
- Install Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bba56240651f789b45c18b006b16e5e07b10676e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217028"
---
# <a name="install-element"></a>Élément d’installation

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

l’élément **Install** spécifie les valeurs utilisées par Lecteur Windows Media pour installer un magasin en ligne.

``` syntax
<Install
    EULAURL = "URL"
    CodeURL = "URL"
    PrivacyInfoURL = "URL"
    InstallApp = "filename"
    InstallData = "commandline"
    CatalogURL = "URL"
/>
```

## <a name="attributes"></a>Attributs

<dl> <dt>

<span id="EULAURL__required_"></span><span id="eulaurl__required_"></span><span id="EULAURL__REQUIRED_"></span>**EULAURL** (obligatoire)
</dt> <dd>

URL complète d’un fichier avec une extension de nom de fichier .txt que Lecteur Windows Media utilise pour afficher un contrat de licence utilisateur final (cluf). Ce fichier doit être encodé au format ANSI.

</dd> <dt>

<span id="CodeURL__required_"></span><span id="codeurl__required_"></span><span id="CODEURL__REQUIRED_"></span>**CodeURL** (obligatoire)
</dt> <dd>

URL complète d’un package, avec une extension de nom de fichier .cab, utilisée pour installer le magasin en ligne. Le package et tous les modules de code du package doivent être signés. Pour plus d’informations sur la signature de code, consultez [Introduction à la signature de code](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) dans MSDN Library.

</dd> <dt>

<span id="PrivacyInfoURL__required_"></span><span id="privacyinfourl__required_"></span><span id="PRIVACYINFOURL__REQUIRED_"></span>**PrivacyInfoURL** (obligatoire)
</dt> <dd>

URL complète d’une page Web qui contient des informations sur les stratégies de confidentialité de la boutique en ligne.

</dd> <dt>

<span id="InstallApp__required_"></span><span id="installapp__required_"></span><span id="INSTALLAPP__REQUIRED_"></span>**InstallApp** (obligatoire)
</dt> <dd>

Nom du fichier EXE ou INF à exécuter. Ce fichier doit être contenu dans le fichier CAB spécifié par l’attribut **CodeURL** .

</dd> <dt>

<span id="InstallData__optional_"></span><span id="installdata__optional_"></span><span id="INSTALLDATA__OPTIONAL_"></span>**InstallData** (facultatif)
</dt> <dd>

Chaîne de ligne de commande qui est transmise à l’application spécifiée par l’attribut **InstallApp** . Cet attribut s’applique uniquement lorsque la valeur de **InstallApp** spécifie un exécutable.

</dd> <dt>

<span id="CatalogURL__required_for_type_1__ignored_for_type_2_"></span><span id="catalogurl__required_for_type_1__ignored_for_type_2_"></span><span id="CATALOGURL__REQUIRED_FOR_TYPE_1__IGNORED_FOR_TYPE_2_"></span>**CatalogURL** (obligatoire pour le type 1, ignoré pour le type 2)
</dt> <dd>

URL complète du catalogue compilé de la boutique en ligne.

</dd> </dl>

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Élément         |
|-----------------|-----------------|
| Éléments parents | **ServiceInfo** |
| Éléments enfants  | None            |



 

## <a name="remarks"></a>Notes

si l’un des attributs requis est manquant ou n’est pas disponible, Lecteur Windows Media installation ne tente pas de télécharger et d’installer le code du fournisseur de la banque d’aide en ligne. Le programme d’installation configure les valeurs par défaut hors connexion comme spécifié dans le document **serviceInfo** . Vous pouvez utiliser **serviceInfo** quand vous n’êtes pas connecté à Internet en passant le nom du fournisseur par défaut et les informations **serviceInfo** en tant que paramètres de ligne de commande. pour plus d’informations sur les options de ligne de commande, consultez [redistribution de Lecteur Windows Media Software](redistributing-windows-media-player-software.md) .

> [!Note]  
> Pour utiliser cet élément, vous devez signer un contrat de redistribution auprès de Microsoft. Pour plus d’informations, contactez votre représentant commercial.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------|
| Version<br/> | Lecteur Windows Media 10 ou version ultérieure.<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Exemple de document ServiceInfo pour une boutique en ligne de type 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Exemple de document ServiceInfo pour un magasin de type 2 en ligne**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Document ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

