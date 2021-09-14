---
title: Charge IAgent
description: Charge IAgent
ms.assetid: 8f25e6b6-a117-4b37-969a-d8f80c7be224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ce2835d60f3edce6f45d181927437ba6e58b18
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414274"
---
# <a name="iagentload"></a>IAgent :: Load

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT Load(
   VARIANT vLoadKey,  // data provider
   long * pdwCharID,  // address of a variable for character ID
   long * pdwReqID    // address of a variable for request ID
);
```

Charge un caractère dans la collection de [**caractères**](./iagent.md) .

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*
</dt> <dd>

Un type de données Variant qui doit être l’un des suivants :



| Valeur           | Description                                                                      |
|------------|-----------------------------------------------------------------------|
| *filespec* | Emplacement du fichier de définition du caractère spécifié dans le fichier local. |
| *URL*      | Adresse HTTP du fichier de définition du caractère.                 |



 

</dd> <dt>

<span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*
</dt> <dd>

Adresse d’une variable qui reçoit l’ID du caractère.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Adresse d’une variable qui reçoit l’ID de la demande de [**chargement**](load-method.md) .

</dd> </dl>

Vous pouvez charger des caractères à partir du sous-répertoire Microsoft Agent en spécifiant un chemin d’accès relatif (un caractère qui n’inclut pas de deux-points ou d’une barre oblique de début). Cela préfixe le chemin d’accès avec le répertoire de caractères de l’agent (situé dans le répertoire% Windows% \\ msagent localisé). Vous pouvez également utiliser une adresse relative pour spécifier votre propre répertoire dans le répertoire de caractères de l’agent.

Vous ne pouvez pas charger le même caractère (un caractère ayant le même GUID) plusieurs fois à partir d’une seule connexion. De même, vous ne pouvez pas charger le caractère par défaut et d’autres caractères en même temps à partir d’une seule connexion, car le caractère par défaut peut être identique à l’autre caractère. Toutefois, vous pouvez créer une autre connexion (à l’aide de CoCreateInstance) et charger le même caractère.

Le fournisseur de données de Microsoft agent prend en charge le chargement de données de caractères stockées sous la forme d’un fichier structuré unique (. ACS) avec les données de caractères et les données d’animation ensemble, ou en tant que données de caractères distinctes (. ACF) et d’animation (. ). En règle générale, utilisez la structure structurée unique. Fichier ACS pour charger un caractère stocké sur un lecteur de disque local ou un réseau et accessible à l’aide du protocole de fichier conventionnel (tel que les chemins d’accès UNC). Utilisez le distinct. ACF et. Les fichiers de CCN lorsque vous souhaitez charger les fichiers d’animation individuellement à partir d’un site distant où ils sont accessibles via le protocole HTTP.

Pour. Les fichiers ACS, à l’aide de la méthode [**Load**](load-method.md) , permettent d’accéder aux animations d’un caractère. une fois chargé, vous pouvez utiliser la méthode [**Play**](play-method.md) pour animer le caractère. Pour. Fichiers ACF, vous utilisez également la méthode [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) pour charger les données d’animation. La méthode **Load** ne prend pas en charge le téléchargement. Fichiers ACS à partir d’un site HTTP.

Le chargement d’un caractère n’affiche pas automatiquement le caractère. Utilisez d’abord la méthode [**Show**](show-method.md) pour rendre le caractère visible.

 

 