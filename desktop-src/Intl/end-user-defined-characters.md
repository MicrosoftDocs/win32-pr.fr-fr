---
description: Les caractères définis par l’utilisateur final (EUDC) dans les jeux de caractères codés sur deux octets (DBCS) et les caractères de zone d’utilisation privée (PUA) en Unicode sont des caractères personnalisés.
ms.assetid: e76ea1ed-5962-440a-a722-b59b314babd6
title: Caractères de zone d’utilisation privée et définis par l’utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19152ff8564cae4ccccc154a6c9d349f0fc6cd8791fcccb1973b553bc681cc5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898758"
---
# <a name="end-user-defined-and-private-use-area-characters"></a>Caractères de zone d’utilisation privée et définis par l’utilisateur

Les caractères définis par l’utilisateur final (EUDC) dans les [jeux de caractères codés sur deux octets](double-byte-character-sets.md) (DBCS) et les caractères de zone d’utilisation privée (PUA) en [Unicode](unicode.md) sont des caractères personnalisés. Elles peuvent être définies et implémentées par un utilisateur final ou par une autre partie, telle qu’un fabricant d’équipements, un groupe d’utilisateurs, un organisme gouvernemental ou une société de conception de polices. Leur utilisation permet aux utilisateurs de former des noms et d’autres mots à l’aide de caractères qui ne sont pas disponibles dans les polices d’écran et d’imprimante standard.

Les caractères EUDC et PUA peuvent être attribués différemment ou non attribués sur des ordinateurs différents. Certaines pages de codes ont des extensions qui réutilisent la plage EUDC, et ces extensions peuvent entrer en conflit. Dans d’autres cas, un fabricant peut fournir un ensemble personnalisé de caractères dans l’une de ces plages. En outre, les groupes d’utilisateurs peuvent tenter de fournir des caractères supplémentaires dans le PUA. Différentes combinaisons de ces cas peuvent entraîner un conflit. Lorsque vous créez des applications qui reposent sur des caractères EUDC ou PUA, vous devez garder à l’esprit les interprétations conflictuelles d’un point de code individuel.

Les rubriques suivantes décrivent les polices qui prennent en charge EUDCs, ainsi que l’accès et la gestion de ces caractères :

-   [Jeux de caractères et polices](character-sets-and-fonts.md)
-   [Entrées de Registre EUDC](eudc-registry-entries.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos d’Unicode et des jeux de caractères](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



