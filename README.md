# Fraction: 一个简单的分数类

支持64位整数(long long)范围内的分数的加减乘除以及混合赋值、输入输出

### 标准输入格式:

> 分子 分母

### 标准输出格式

> 分子/分母

### 公开成员函数说明

  bool IsInteger();
  
  判断分数的当前值是不是整数。
	
  double ToDouble();
  
  将分数转换为浮点数。
	
  long long ToInt(bool bCeil);
  
  将分数转换为整数。根据bCeil的取值决定是向下取整还是向上取整。
	
  Fraction Numden(Fraction &fracFraction);
  
  将分数与另一个分数通分。
	
  Fraction Reduction();
  
  将当前分数越分。
	
  void SetValue(long long iNumerator, long long iDenominator);
  
  通过确定的分子与分母来给分数赋值。
	
  void SetValue(long long iNum);
  
  通过一个确定的整数给分数赋值。
	
  long long GetNumerator();
  
  获取分子的值。
	
  long long GetDenominator();
  
  获取分母的值。
  
  static Fraction Reduction(Fraction fracFraction);
  
  静态成员函数，对给定的分数进行越分。

### 公开成员变量说明
	
  static bool bIgnoreDivideZeroErrors;
  
  是否忽略分母为零的错误。
  
  > _FRACTION_ZERO_DIVIDE_ERROR_LEVEL_WARN 0 提示出错
  
  > _FRACTION_ZERO_DIVIDE_ERROR_LEVEL_ABORT 1提示出错并终止
	
  static int iErrInputDenominatorZeroErrors;
  
  对于除零错误的处理方式。
  
  > _FRACTION_ZERO_DENOMINATOR_ERROR_LEVEL_NOERR 0 不处理
  
  > _FRACTION_ZERO_DENOMINATOR_ERROR_LEVEL_WARN 1 提示出错
  
  > _FRACTION_ZERO_DENOMINATOR_ERROR_LEVEL_ABORT 2 提示出错并终止
