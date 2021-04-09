---
title: Inscription de l’extension de création d’objet
description: Quand une DLL d’extension de création d’objet est créée dans Active Directory Domain Services, elle doit être inscrite auprès du Registre Windows et Active Directory Domain Services pour que COM et les composants logiciels enfichables MMC d’administration Active Directory prennent en compte l’extension.
ms.assetid: 6e950c6c-1a4f-4de0-9be1-004c31d4734c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27d8e2a50c2340d678fd43e546d68525afbc8a7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103940800"
---
# <a name="registering-the-object-creation-extension"></a>Inscription de l’extension de création d’objet

Quand une DLL d’extension de création d’objet est créée dans Active Directory Domain Services, elle doit être inscrite auprès du Registre Windows et Active Directory Domain Services pour que COM et les composants logiciels enfichables MMC d’administration Active Directory prennent en compte l’extension.

## <a name="registering-in-the-windows-registry"></a>Inscription dans le Registre Windows

Comme tous les serveurs COM, une extension de création d’objet doit être inscrite dans le Registre Windows. L’extension est inscrite sous la clé suivante :

```
HKEY_CLASSES_ROOT
   CLSID
      <extension CLSID>
         InProcServer32
            (Default) = <extension path>
            ThreadingModel = Apartment
```

« &lt; CLSID &gt; d’extension » est la représentation sous forme de chaîne du CLSID telle qu’elle est produite par la fonction [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) . « &lt; chemin d’accès &gt; de l’extension » contient le chemin d’accès et le nom de fichier de la dll d’extension. La valeur **ThreadingModel** pour toutes les extensions de création d’objet doit être « Apartment ».

## <a name="registering-with-active-directory-domain-services"></a>Inscription avec Active Directory Domain Services

L’inscription de l’extension de création d’objet est spécifique à un paramètre régional. Si l’extension de création d’objet s’applique à tous les paramètres régionaux, elle doit être inscrite dans l’objet **displaySpecifier** de la classe d’objets dans tous les sous-conteneurs de paramètres régionaux du conteneur DisplaySpecifiers. Si l’extension de création d’objet est localisée pour certains paramètres régionaux, inscrivez-la dans l’objet **displaySpecifier** dans le sous-conteneur de ces paramètres régionaux. Pour plus d’informations sur le conteneur DisplaySpecifiers et les paramètres régionaux, consultez [spécificateurs d’affichage](display-specifiers.md) et [conteneur DisplaySpecifiers](displayspecifiers-container.md).

Il existe deux attributs DisplaySpecifier sous lesquels une extension de création d’objet peut être inscrite. Il s’agit de **creationWizard** et **createWizardExt**.

L’attribut **creationWizard** identifie les extensions de création d’objet principal pour remplacer l’Assistant Création d’objet existant ou natif dans Active Directory composants logiciels enfichables d’administration. Une extension de création principale fournit le premier ensemble de pages et est hébergée de la même façon que les pages natives. Cet attribut est à valeur unique et requiert le format suivant :


```C++
<CLSID>
```



Le &lt; CLSID &gt; est la représentation sous forme de chaîne du CLSID de l’objet com, tel qu’il est généré par la fonction [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .

L’attribut **createWizardExt** identifie les extensions de création d’objets secondaires. Une extension de création secondaire ajoute des pages d’assistant aux pages natives ou à l’extension principale. Cet attribut est à valeurs multiples et requiert le format suivant :


```C++
<order number>,<CLSID>
```



« &lt; Order Number &gt; » est un nombre non signé qui représente la position de la page dans l’Assistant. Quand un assistant de création est affiché, les valeurs sont triées à l’aide d’une comparaison entre le « numéro d’ordre » de chaque valeur &lt; &gt; . Si plusieurs valeurs ont le même « numéro de &lt; commande &gt; », ces pages sont chargées dans l’ordre dans lequel elles sont lues à partir du serveur de Active Directory. Si possible, vous devez utiliser un « &lt; numéro d’ordre » non existant &gt; (autrement dit, un numéro qui n’a pas été utilisé par d’autres valeurs de la propriété). Il n’y a pas de position de départ prescrite, et les espaces sont autorisés dans la &lt; séquence « Order Number &gt; ».

Le &lt; CLSID &gt; est la représentation sous forme de chaîne du CLSID de l’objet com, tel qu’il est généré par la fonction [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .

 

 