---
description: Les opérations privilégiées requièrent des privilèges de sécurité tels que SeLoadDriverPrivilege (wbemPrivilegeLoadDriver dans les constantes de l’API de script), un privilège qui doit être activé pour un compte qui charge un pilote de périphérique.
ms.assetid: 11bb8723-f329-4083-8219-2256ce44a5e3
ms.tgt_platform: multiple
title: Exécution des opérations privilégiées
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce87a5783462be86d6e2e2b0565e93d811b972393319a34f84be2ab3d8e34c64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050867"
---
# <a name="executing-privileged-operations"></a>Exécution des opérations privilégiées

Les opérations privilégiées requièrent des privilèges de sécurité tels que **SeLoadDriverPrivilege** (**WbemPrivilegeLoadDriver** dans les [constantes](scripting-api-constants.md)de l’API de script), un privilège qui doit être activé pour un compte qui charge un pilote de périphérique. Vous ne pouvez pas ajouter de privilèges à un administrateur ou à un utilisateur par le biais de WMI. vous pouvez uniquement activer les privilèges que le compte possède déjà. Pour obtenir la liste des privilèges, [**consultez \_ constantes de privilège**](privilege-constants.md).

Par défaut, un utilisateur local sur un ordinateur peut lire des données statiques à partir de l' [*espace de stockage WMI*](gloss-w.md), écrire dans des instances fournies par des fournisseurs et exécuter des méthodes de fournisseur, sauf si le fournisseur applique des exigences de sécurité spécifiques. Seuls les administrateurs peuvent [se connecter à un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md), modifier les descripteurs de sécurité ou modifier les données de référentiel WMI statiques, telles qu’une définition de classe WMI. Tous les privilèges sont activés pour une connexion à distance. Pour plus d’informations, consultez [sécurisation d’une connexion WMI à distance](securing-a-remote-wmi-connection.md).

Les constantes de privilège pour C++ diffèrent de celles utilisées par les langages Automation tels que Visual Basic. Les scripts doivent utiliser la valeur de la constante plutôt que le nom. Pour plus d’informations, consultez [exécution d’opérations privilégiées à l’aide de C++](executing-privileged-operations-using-c-.md) ou exécution d' [opérations privilégiées à l’aide de VBScript](executing-privileged-operations-using-vbscript.md).

La cause courante des erreurs de refus d’accès lors de l’utilisation de WMI est l’absence de privilège activé pour les opérations, comme l’obtention de toutes les instances de [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)). Si vous n’activez pas le privilège de **sécurité** , vous ne pouvez pas accéder au fichier journal de sécurité.

L’exemple de code VBScript suivant montre comment définir le privilège **sesecurity** dans la chaîne de moniker. En cas d’utilisation dans le moniker, le nom de privilège entre parenthèses supprime le « se » initial. Pour plus d’informations, consultez [construction d’une chaîne de moniker](constructing-a-moniker-string.md).


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate,(Security)}!\\" _
    & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery _
    ("Select * from Win32_NTEventLogFile " _
    & "Where LogFileName='Security'")
For Each LogFile in colFiles
Wscript.Echo LogFile.NumberOfRecords
Next
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Constantes de privilège**](privilege-constants.md)
</dt> </dl>

 

 
