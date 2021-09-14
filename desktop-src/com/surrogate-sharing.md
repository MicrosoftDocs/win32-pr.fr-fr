---
title: Partage de substitution
description: Les serveurs DLL partagent un substitut s’ils ont des identités de sécurité correspondantes et partagent la même valeur AppID.
ms.assetid: 88544be1-4716-47b6-9c08-2b5b2b178e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6a934f03d42113cf73df4f059ac108801d21ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127221780"
---
# <a name="surrogate-sharing"></a>Partage de substitution

Les serveurs DLL partagent un substitut s’ils ont des identités de sécurité correspondantes et partagent la même valeur AppID.

Les serveurs DLL sont chargés, par défaut, dans leur propre processus de substitution. Pour charger d’autres serveurs DLL dans un substitut existant afin qu’il prenne en charge plusieurs serveurs DLL, deux conditions sont requises :

-   Les serveurs DLL doivent avoir la même valeur AppID.
-   Le contexte de sécurité des serveurs DLL doit être le même.

Si deux serveurs DLL doivent être lancés sous différentes identités de sécurité, ils doivent être dans des substituts différents, que leurs AppID correspondent.

Voici un exemple d’administration du partage de substitution avec les AppID :

``` syntax
    AppID
        {12345678-0000-0000-0000-abcdabcdabcd}
            @DllSurrogate    REG_SZ
    CLSID
        {12345678-0000-0000-0000-000000000001}
            @AppId    REG_SZ    {12345678-0000-0000-0000-abcdabcdabcd}
            InProcServer32
    @    REG_SZ    c:\myapp\comp1.dll
        {12345678-0000-0000-0000-000000000002}
            @AppId    REG_SZ    {12345678-0000-0000-0000-abcdabcdabcd}
            InProcServer32
    @    REG_SZ    c:\myapp\comp2.dll
 
```

Les deux CLSID des composants DLL comp1.dll et comp2.dll ont été configurés pour partager une AppID. La clé [AppID](appid-key.md) spécifie que le serveur dll peut être chargé dans un substitut en spécifiant la valeur [DllSurrogate](dllsurrogate.md) . Dans cet exemple, la valeur **DllSurrogate** est une chaîne vide, ce qui indique que l’implémentation système par défaut du substitut de la dll doit être utilisée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration requise du serveur DLL](dll-server-requirements.md)
</dt> <dt>

[Inscription du serveur DLL pour l’activation du remplacement](registering-the-dll-server-for-surrogate-activation.md)
</dt> </dl>

 

 




