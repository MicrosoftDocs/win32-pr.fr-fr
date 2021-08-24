---
description: Lors de l’installation d’un fournisseur de réseau, votre application doit créer les clés de Registre et les valeurs décrites dans cette rubrique.
ms.assetid: cc5a4a7b-02b5-4ecd-967c-de0656f00846
title: Clés de registre d’authentification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c245cdb27a0d661e7e6df82ed0d1d0ed35a59ea05bf74bf98ebd39ba3dc791
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883679"
---
# <a name="authentication-registry-keys"></a>Clés de registre d’authentification

Lors de l’installation d’un fournisseur de réseau, votre application doit créer les clés de Registre et les valeurs décrites dans cette rubrique. Ces clés et ces valeurs fournissent des informations à l’MPR sur les fournisseurs de réseau installés sur le système. Le service MPR vérifie ces clés lorsqu’il démarre et charge les dll du fournisseur réseau qu’il trouve.

Avant de créer un ensemble de clés pour stocker des informations sur votre fournisseur réseau, vous devez ajouter le nom de votre fournisseur de réseau à la clé de **commande** . Cette clé est une sous-clé de la clé suivante :

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
```

La clé de **commande** contient une valeur unique, **ProviderOrder**, qui répertorie les fournisseurs installés et spécifie l’ordre dans lequel ils doivent être essayés pendant les opérations qui traversent les fournisseurs jusqu’à ce qu’un fournisseur acceptant soit trouvé.

La valeur **ProviderOrder** contient une liste de noms de clés séparés par des virgules. Chaque nom de clé dans **ProviderOrder** identifie un fournisseur réseau. Lorsque MPR parcourt les fournisseurs, il les appelle dans l’ordre dans lequel ils apparaissent dans cette liste.

Le nom de fournisseur défini dans **ProviderOrder** doit également être utilisé comme nom de la clé de Registre qui contient des informations sur ce fournisseur. Les clés de Registre spécifiques au fournisseur sont créées en tant que sous-clés de la clé suivante :

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

En d’autres termes, les noms de fournisseurs spécifiés dans **ProviderOrder** sont le chemin d’accès au registre des clés spécifiques au fournisseur de réseau, par rapport au chemin d’accès suivant :

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

Lorsque votre service de fournisseur de réseau est installé, l’application d’installation doit ajouter une clé comme suit :

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            ProviderName
```

Où *providerName* est le nom du fournisseur réseau, tel que spécifié dans la valeur **ProviderOrder** de la clé de **commande** . La valeur de **groupe** sous la clé *providerName* doit être définie sur « NetworkProvider ». Cela identifie le service comme étant dans le groupe de fournisseurs de réseau.

Vous devez également créer une sous-clé de *providerName*, **NetworkProvider**. Cette clé contient les valeurs suivantes qui décrivent le fournisseur réseau.



| Valeur                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nom**<br/>         | Contient le nom du fournisseur. Ce nom est affiché pour l’utilisateur en tant que nom du réseau dans les boîtes de dialogue de navigation et doit correspondre au champ **lpProvider** renvoyé dans les structures de [**ressources**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) réseau. Ce nom doit être une variante du nom du produit, de préférence avec une certaine indication de la société, afin qu’elle soit claire et unique. « MS-LanMan », par exemple, est un bon nom, tandis que « The net » est un mauvais choix.<br/> |
| **ProviderPath**<br/> | Contient le chemin d’accès complet de la DLL qui implémente le fournisseur réseau. MPR appelle [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) sur ce chemin d’accès.<br/>                                                                                                                                                                                                                                                                                                                                |



 

Les valeurs suivantes sont utilisées uniquement par les fournisseurs de réseau qui prennent en charge les fonctions de gestion des informations d’identification, [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) et [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify).



| Valeur                              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Classe**<br/>               | **Valeur DWORD** qui identifie la classe, ou le type, de la fonctionnalité de fournisseur prise en charge par ce fournisseur. Les valeurs peuvent être jointes par l’opérateur **or** , le cas échéant. Les valeurs valides sont : WN \_ Network, classe, la classe \_ \_ Credential WN, la \_ \_ \_ classe AUTHENT principale WN et la \_ \_ classe de service WN \_ .<br/> Bien qu’un fournisseur puisse prendre en charge la fonctionnalité d’authentificateur principal, un autre moyen sera utilisé pour déterminer quel authentificateur est principal.<br/> **Windows XP/2000 :** Le changement d’authentificateurs principal n’est pas pris en charge. cette valeur est donc ignorée. <br/> |
| **AuthentProviderPath**<br/> | Il s’agit du nom de fichier complet de la DLL qui exporte les fonctions de gestion des informations d’identification. Cette valeur est utile (mais pas obligatoire) uniquement lorsque le fournisseur est identifié comme étant une classe d’informations d’identification \_ ou un \_ fournisseur de classe AUTHENT primaire \_ . Si cette valeur n’est pas présente pour un fournisseur de cette classe, les fonctions de gestion des informations d’identification doivent être exportées à partir de la DLL identifiée par la valeur ProviderPath. Cette valeur est utilisée uniquement s’il est souhaitable d’empaqueter les fonctions réseau et les fonctions du gestionnaire d’informations d’identification dans des dll distinctes.<br/>  |



 

Outre les valeurs utilisées pour enregistrer les fournisseurs de réseau et les gestionnaires d’informations d’identification, vous pouvez ajouter une valeur au registre pour inscrire une DLL afin de recevoir des notifications de connexion. Pour ce faire, créez une \_ valeur de \_ la valeur SZ reg Expand sous la clé suivante :

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
               Notifyees
```

Cette valeur doit spécifier le chemin d’accès à une DLL qui implémente l' [API de notification de connexion](connection-notification-api.md). Le nom de cette valeur peut être tout ce que vous voulez, à condition qu’il n’entre pas en conflit avec les noms de valeurs préexistants.

## <a name="example"></a>Exemple

L’exemple suivant montre les clés de Registre pour un système sur lequel deux fournisseurs de réseau sont installés : LanmanWorkStation et AnotherNetSvc. AnotherNetSvc est également un gestionnaire d’informations d’identification. Dans l’exemple, les noms de clé sont en gras et les noms de valeur sont en italique.

**HKEY \_ \_** \\  \\  \\  \\  \\ **Ordre** NetworkProvider du contrôle CurrentControlSet du système de l’ordinateur local

*ProviderOrder* = "LanmanWorkStation, AnotherNetSvc"

**HKEY \_ \_** \\  \\  \\  \\  \\ **Notifications** de contrôles CurrentControlSet du système d’ordinateur local NetworkProvider

*MyNotifyApp* = "c : \\ Connect \\connect.dll"

**HKEY \_ \_** \\  \\  \\ **Services** de CurrentControlSet de système \\  d’ordinateur local LanmanWorkStation\\

*Groupe* = « NetworkProvider »

**HKEY \_ Services d' \_ ordinateur local** \\ **système** de \\ **CurrentControlSet** \\  \\  \\ **NetworkProvider** LanmanWorkStation

*Name* = "NT LanMan"*ProviderPath* = "ntlanman.dll"

*Class* = 0x00000001 ( \_ classe réseau WN \_ )

**HKEY \_ \_** \\  \\  \\ **Services** de CurrentControlSet de système \\  d’ordinateur local AnotherNetSvc\\

*Groupe* = « NetworkProvider »

**HKEY \_ \_** Services de CurrentControlSet de système d’ordinateur local \\  \\  \\  \\ **AnotherNetSvc** \\ **NetworkProvider**

*Name* = "un autre réseau"*ProviderPath* = "c : \\ un autre \\anet.dll"

*Class* = 0x00000003 (classe \_ \_ \| \_ d’informations d’identification \_ de la classe de réseau Wn)

*AuthentProviderPath* = "c : \\ autre \\anetCM.dll"

 

