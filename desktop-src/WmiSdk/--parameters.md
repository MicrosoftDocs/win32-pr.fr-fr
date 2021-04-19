---
description: Définit les paramètres d’entrée et de sortie des méthodes.
ms.assetid: d973feb5-27c4-4d8e-bf1b-0a455afa4375
ms.tgt_platform: multiple
title: Classe __PARAMETERS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PARAMETERS
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: df858445797a45e21a0d54e9aedc2387851ae54f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527934"
---
# <a name="__parameters-class"></a>\_\_Parameters, classe

La classe de système **\_ \_ Parameters** est une classe abstraite qui définit les paramètres d’entrée et de sortie des méthodes. Il est également utilisé pour passer des valeurs de paramètre d’entrée et de sortie entre un client WMI et un fournisseur de méthode.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[abstract]
class __PARAMETERS
{
};
```

## <a name="members"></a>Membres

La classe **\_ \_ Parameters** ne définit aucun membre.

## <a name="remarks"></a>Notes

Pour définir une méthode dans une classe d’utilisateur, un client WMI crée une copie de la classe de **\_ \_ paramètres** et ajoute une propriété pour chaque paramètre d’entrée dans une méthode. Si la méthode contient une valeur de retour ou des paramètres de sortie, une autre copie des **\_ \_ paramètres** doit être créée. Si la méthode retourne une valeur de retour, le client doit ajouter une propriété nommée **returnValue**. Le fournisseur de méthode stocke ensuite les paramètres de méthode avec un appel à [**IWbemClassObject ::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).

Pour appeler une méthode, un client appelle les éléments suivants dans l’ordre :

1.  [**IWbemClassObject :: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) pour récupérer une copie de la classe de **\_ \_ paramètres** qui est stockée par [**IWbemClassObject ::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).
2.  [**IWbemClassObject :: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance), puis définit une propriété pour chaque paramètre d’entrée de la méthode.
3.  [**IWbemServices :: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) ou [**IWbemServices :: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) pour exécuter la méthode.

Une fois l’exécution de la méthode terminée, une autre instance de la classe **\_ \_ Parameters** peut être retournée si la méthode a des paramètres de sortie ou une valeur de retour.

-   Si la méthode a été appelée à l’aide de [**IWbemServices :: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), l’instance des **\_ \_ paramètres** est retournée en tant qu’argument de sortie.
-   Si la méthode a été appelée à l’aide de [**IWbemServices :: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), l’instance de **\_ \_ paramètres** est retournée en tant que paramètre à [**IWbemObjectSink :: indique**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> <dt>

[**IWbemServices :: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[Appel d’une méthode](calling-a-method.md)
</dt> </dl>

 

 




