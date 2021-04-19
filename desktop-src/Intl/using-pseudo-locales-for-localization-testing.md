---
description: Sur Windows Vista et versions ultérieures, vous pouvez utiliser des pseudo-paramètres régionaux pour tester l’adaptabilité des applications. Cette rubrique comprend des procédures pour l’utilisation de Pseudo-codes.
ms.assetid: 1eccdbb9-a1bd-443a-a5f6-d64c9e5c87b3
title: Utilisation de Pseudo-paramètres régionaux pour le test d’adaptabilité
ms.topic: article
ms.date: 07/05/2018
ms.openlocfilehash: f8c6b435b85a5bef98eff9bf76681096779433e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539761"
---
# <a name="using-pseudo-locales-for-localizability-testing"></a>Utilisation de Pseudo-paramètres régionaux pour le test d’adaptabilité

Les [Pseudo-paramètres régionaux](pseudo-locales.md) sont intégrés à Windows Vista et versions ultérieures, afin que vous puissiez y accéder via les API NLS (National Language Support). Vous pouvez utiliser des pseudo-paramètres régionaux pour tester l' [adaptabilité](/windows/uwp/design/globalizing/globalizing-portal) de vos applications. Cette rubrique comprend des procédures pour l’utilisation de Pseudo-codes.

> [!NOTE]
> Une tâche nécessitant une attention particulière en ce qui concerne les pseudo-paramètres régionaux consiste à les énumérer. Si vous êtes dans votre code, ou dans la partie Options régionales et linguistiques du panneau de configuration. Plus loin dans cette rubrique.

Les noms des pseudo-paramètres régionaux sont « RPS-Ploc », « RPS-Ploca » et « RPS-plocm ». À compter de Windows 10, les pseudo-paramètres régionaux « RPS-LATN-x-SH » sont également disponibles.

## <a name="retrieve-information-about-pseudo-locales"></a>Récupérer les informations sur les pseudo-paramètres régionaux

Vous pouvez utiliser [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) pour récupérer des informations sur les pseudo-paramètres régionaux. Transmettez à la fonction le nom des pseudo-paramètres régionaux particuliers (consultez la liste des noms ci-dessus). Par exemple, « RPS-plocm » pour les pseudo-paramètres régionaux en miroir.

```cpp
wchar_t languageIdentifier[5];
int rc{ ::GetLocaleInfoEx(L"qps-plocm", LOCALE_ILANGUAGE, languageIdentifier, 5) };
```

## <a name="use-localenametolcid-with-pseudo-locales"></a>Utiliser LocaleNameToLCID avec Pseudo-paramètres régionaux

Vous pouvez appeler la fonction de mappage NLS [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) avec le nom d’un pseudo-paramètres régionaux.

```cpp
LCID lcid{ ::LocaleNameToLCID(L"qps-plocm", 0) };
```

## <a name="enable-pseudo-locales-for-enumeration"></a>Activer les pseudo-paramètres régionaux pour l’énumération

Dans votre application, vous pouvez appeler [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) pour énumérer les paramètres régionaux reconnus par le système. La partie Options régionales et linguistiques du panneau de configuration appelle également **EnumSystemLocalesEx** pour générer la liste des paramètres régionaux qu’elle affiche. Toutefois, par défaut, les quatre Pseudo-paramètres régionaux répertoriés ci-dessus ne sont pas reconnus par le système, donc ils ne sont pas retournés par **EnumSystemLocalesEx**. Pour les systèmes Windows Vista jusqu’à Windows 10, version 1709, la solution consiste à activer les pseudo-paramètres régionaux en ajoutant des clés au registre Windows.

Les modifications sont apportées sous la \_ \_ clé nls du contrôle du système d’exploitation de la machine locale HKEY \\ \\ \\ \\ pour les langues installées sur le système d’exploitation. Vous pouvez définir ces paramètres pour activer les pseudo-paramètres régionaux. Chaque clé indiquée ci-dessous est le LCID hexadécimal correspondant aux pseudo-paramètres régionaux en cours d’activation. Chaque valeur est de type chaîne (REG \_ SZ).

```
[HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Nls\Locale]
"00000501"="1" // qps-ploc (Windows Vista and later)
"000005fe"="7" // qps-ploca (Windows Vista and later)
"00000901"="1" // qps-Latn-x-sh (Windows 10 and later)
"000009ff"="d" // qps-plocm (Windows Vista and later)
```

Pour Windows 10, version 1803, la modification du Registre Windows comme celle-ci n’a aucun effet. Toutefois, vous pouvez toujours appeler les API NLS sans énumération avec les noms des pseudo-paramètres régionaux (voir les exemples de code ci-dessus) pour renseigner votre interface utilisateur.

## <a name="related-topics"></a>Rubriques connexes

* [Utilisation de la prise en charge linguistique nationale](using-national-language-support.md)
* [Pseudo-paramètres régionaux](pseudo-locales.md)
* [EnumSystemLocalesEx](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex)
* [GetLocaleInfoEx](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
* [LocaleNameToLCID](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
